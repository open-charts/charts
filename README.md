# Open Charts - Community-Driven Helm Charts

> A community-maintained fork of essential Helm charts, born from the need for open and accessible Kubernetes application deployments.

## Why Open Charts?

In 2025, Broadcom announced that Bitnami Helm Charts would be migrated to a paid subscription model, with legacy charts being deleted after August 28th, 2025. This represents a significant shift from the open-source ethos that made Bitnami charts a cornerstone of the Kubernetes ecosystem.

**The question posed to our community was simple:** *"Can we as a community afford to fork AND, more importantly, maintain them?"*

**Our answer:** Yes, we can and we must.

Open Charts represents our commitment to keeping essential Kubernetes deployment tools freely available to everyone. We believe that infrastructure tooling should remain open and accessible, enabling developers and organizations of all sizes to deploy applications on Kubernetes without vendor lock-in or subscription barriers.

## What We Offer

Open Charts provides community-maintained versions of popular application charts:

- **MySQL** - Relational database management system
- **PostgreSQL** - Advanced open-source relational database
- **Redis** - In-memory data structure store
- **NGINX** - High-performance web server and reverse proxy
- **RabbitMQ** - Message broker for distributed systems

All charts are:
- ✅ Free and open source (MIT licensed)
- ✅ Actively maintained by the community
- ✅ Compatible with existing Bitnami chart configurations
- ✅ Hosted on GitHub Container Registry (ghcr.io)
- ✅ Available via GitHub Pages Helm repository

## Quick Start

### Adding the Repository

```bash
helm repo add open-charts https://open-charts.github.io/charts
helm repo update
```

### Installing Charts

```bash
# MySQL
helm install my-mysql open-charts/mysql

# PostgreSQL
helm install my-postgres open-charts/postgresql

# NGINX
helm install my-nginx open-charts/nginx

# Redis
helm install my-redis open-charts/redis

# RabbitMQ
helm install my-rabbitmq open-charts/rabbitmq
```

## Migration from Bitnami

If you're currently using Bitnami charts, migrating to Open Charts is straightforward:

1. The chart names and configurations remain largely compatible
2. Update your `helm repo` to point to Open Charts
3. Update image references if using custom registries
4. Test in a non-production environment first

## Contributing

Open Charts is a community effort, and we welcome contributions! Here's how you can help:

- **Report Issues**: Found a bug? Let us know!
- **Submit PRs**: Improvements and fixes are always welcome
- **Documentation**: Help us improve our docs
- **Testing**: Test charts and report your findings
- **Maintenance**: Adopt a chart and help maintain it

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## Sustainability

Unlike venture-backed projects that can be acquired and monetized, Open Charts is designed for long-term sustainability:

- **Community Governance**: Major decisions are made by the community
- **Distributed Maintenance**: No single point of failure
- **Transparent Operations**: All discussions and decisions happen in the open
- **Fork-Friendly**: If needed, anyone can fork and continue the work

## Images

All container images are hosted on GitHub Container Registry (ghcr.io) under the `open-charts` organization:

- `ghcr.io/open-charts/mysql`
- `ghcr.io/open-charts/postgresql`
- `ghcr.io/open-charts/nginx`
- `ghcr.io/open-charts/redis`
- `ghcr.io/open-charts/rabbitmq`

## License

Open Charts is released under the [MIT License](LICENSE), ensuring it remains free and open forever.

## Acknowledgments

We acknowledge the tremendous work done by the Bitnami team over the years. Their charts have been instrumental in making Kubernetes accessible to millions of developers. Open Charts aims to continue this legacy in the true spirit of open source.

## Join Us

The strength of open source lies in its community. Whether you're a developer, DevOps engineer, or just someone who believes in open infrastructure, there's a place for you in Open Charts.

- **GitHub**: [github.com/open-charts/charts](https://github.com/open-charts/charts)
- **Discussions**: [GitHub Discussions](https://github.com/open-charts/charts/discussions)
- **Issues**: [GitHub Issues](https://github.com/open-charts/charts/issues)

---

*"The best way to predict the future is to create it."* - Let's build an open future for Kubernetes deployments together.