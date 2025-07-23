# Contributing to Open Charts

First off, thank you for considering contributing to Open Charts! It's people like you that make Open Charts a sustainable alternative to proprietary solutions.

## Why We Need You

Open Charts was born from a community need - to keep essential Kubernetes deployment tools free and accessible. Every contribution, no matter how small, helps ensure that developers worldwide can continue deploying applications without barriers.

## How Can I Contribute?

### Reporting Bugs

Found something that doesn't work? Please let us know!

- **Check existing issues** first to avoid duplicates
- **Use the bug report template** when creating an issue
- **Include reproduction steps** and your environment details
- **Share logs and error messages** (sanitize sensitive data first)

### Suggesting Enhancements

Have ideas for improvements? We'd love to hear them!

- **Check if it's already suggested** in issues or discussions
- **Explain the use case** - why is this enhancement valuable?
- **Be open to feedback** - the community might have insights

### Code Contributions

Ready to dive into code? Here's how:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-improvement`)
3. **Make your changes**
4. **Test thoroughly** - charts affect production workloads!
5. **Commit with clear messages** (`git commit -m 'Add X to improve Y'`)
6. **Push to your fork** (`git push origin feature/amazing-improvement`)
7. **Open a Pull Request**

#### Pull Request Guidelines

- **One PR = One Feature/Fix** - Keep PRs focused
- **Update documentation** - If you change behavior, update the docs
- **Add tests if applicable** - Help us maintain quality
- **Follow existing patterns** - Consistency matters
- **Be patient** - Reviews take time but ensure quality

### Chart Maintenance

Want to adopt a chart? Chart maintainers:

- Monitor issues related to their chart
- Review PRs affecting their chart
- Keep dependencies updated
- Ensure security patches are applied
- Communicate breaking changes clearly

Contact us in discussions if you'd like to maintain a chart!

### Documentation

Documentation is crucial for adoption:

- Fix typos and clarify confusing sections
- Add examples for common use cases
- Translate documentation to other languages
- Improve installation and migration guides

## Development Setup

### Prerequisites

- Helm 3.x
- Docker (for testing)
- Kubernetes cluster (minikube, kind, or cloud)

### Testing Charts

```bash
# Lint a chart
helm lint charts/mysql

# Test installation
helm install test-mysql charts/mysql --dry-run --debug

# Package chart
helm package charts/mysql
```

## Style Guidelines

### Helm Charts

- Use semantic versioning for chart versions
- Follow Helm best practices
- Include comprehensive values.yaml comments
- Provide values.schema.json for validation
- Document all parameters in README

### Commit Messages

- Use present tense ("Add feature" not "Added feature")
- Keep first line under 50 characters
- Reference issues and PRs (#123)
- Explain *why* not just *what*

## Community

### Code of Conduct

- Be respectful and inclusive
- Welcome newcomers and help them get started
- Focus on what's best for the community
- Show empathy towards other community members

### Getting Help

- **GitHub Discussions**: Ask questions and share ideas
- **Issue Tracker**: Report bugs and request features
- **Pull Requests**: Contribute code and review others' contributions

## Recognition

All contributors are recognized in our:
- GitHub contributors page
- Release notes
- Annual community report

## Questions?

Feel free to ask in [GitHub Discussions](https://github.com/open-charts/charts/discussions). We're here to help!

---

Remember: Open Charts exists because people like you believe in open infrastructure. Every contribution makes a difference!