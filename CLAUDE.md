# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Structure

This is the Open Charts repository, containing Helm charts for popular applications. The repository is organized as follows:

```
charts/
├── common/          # Helm Library Chart with shared template helpers
├── mysql/          # MySQL database chart
├── nginx/          # NGINX web server chart  
├── postgresql/     # PostgreSQL database chart
├── rabbitmq/       # RabbitMQ message broker chart
└── redis/          # Redis cache chart
```

## Common Patterns

### Chart Structure
Each chart follows the standard Helm chart structure:
- `Chart.yaml` - Chart metadata and dependencies
- `values.yaml` - Default configuration values
- `values.schema.json` - JSON schema for values validation
- `templates/` - Kubernetes resource templates
- `README.md` - Chart documentation with parameters table

### Template Helpers
The `common` chart provides shared template helpers used across all charts:
- Naming functions (`common.names.*`)
- Label generators (`common.labels.*`) 
- Image handling (`common.images.*`)
- Storage class management (`common.storage.*`)
- Security contexts and capabilities
- Validation helpers
- Affinity and scheduling helpers

### Key Files to Understand
- `charts/common/templates/` - Contains all shared template helpers
- Individual chart `templates/_helpers.tpl` - Chart-specific template functions
- `values.yaml` files contain extensive configuration options for each service

## Development Commands

Since this is a Helm charts repository, standard commands include:

```bash
# Install dependencies for a chart
helm dependency update charts/mysql

# Lint a chart
helm lint charts/mysql

# Template a chart (dry-run)
helm template my-release charts/mysql

# Package a chart
helm package charts/mysql

# Test chart templates
helm unittest charts/mysql  # if unittest plugin is installed
```

## Architecture Notes

### Dependencies
- All application charts depend on the `common` library chart
- Charts use OCI registry format: `oci://registry-1.docker.io/opencharts`
- The common chart provides standardized Kubernetes resource templates

### Configuration Patterns
- Extensive use of `.Values` hierarchy for configuration
- Security contexts are standardized across charts
- Resource presets available via `resourcesPreset` values
- Support for existing secrets, ConfigMaps, and PVCs
- Network policies and RBAC configurations included

### Template Organization
- Primary/secondary architecture for database charts (MySQL, PostgreSQL, Redis)
- Separate templates for different resource types (StatefulSet, Service, ConfigMap, etc.)
- Modular approach with helper templates for reusability

## Chart-Specific Notes

### MySQL Chart
- Supports both standalone and replication architectures
- Includes metrics export via mysqld_exporter
- Password update job for credential rotation
- TLS support with auto-generation options

### Common Library Chart
This chart provides essential template helpers used by all other charts. Key helper categories:
- Affinities, Capabilities, Images, Ingress, Labels, Names
- Resources, Secrets, Storage, Validations, Warnings
- Special input schemas for ImageRoot, Persistence, ExistingSecret

When working with any chart, always check the common chart's README.md for available helpers and their expected input formats.