# Lareira Helm Charts

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Helm](https://img.shields.io/badge/Helm-v3-informational?logo=helm)](https://helm.sh)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-1.20+-blue.svg?logo=kubernetes)](https://kubernetes.io)

A collection of Helm charts maintained by Lareira for deploying applications on Kubernetes clusters.

## 📋 Table of Contents

- [Prerequisites](#-prerequisites)
- [Repository Structure](#-repository-structure)
- [Usage](#-usage)
- [Available Charts](#-available-charts)
- [Installation](#-installation)
- [Development](#-development)
- [Contributing](#-contributing)
- [Support](#-support)

## 🔧 Prerequisites

Before using these charts, ensure you have the following tools installed:

- [Kubernetes](https://kubernetes.io/) 1.20+
- [Helm](https://helm.sh/) v3.0+
- [kubectl](https://kubectl.docs.kubernetes.io/) configured for your cluster

## 📁 Repository Structure

```
charts/
├── charts/                    # Individual chart directories
│   ├── chart-name/
│   │   ├── Chart.yaml        # Chart metadata
│   │   ├── values.yaml       # Default values
│   │   ├── templates/        # Kubernetes manifests
│   │   └── README.md         # Chart-specific documentation
├── docs/                     # Documentation
├── scripts/                  # Helper scripts
└── README.md                # This file
```

## 🚀 Usage

### Adding the Helm Repository

```bash
# Add the repository (when published)
helm repo add lareira https://lareira.github.io/charts

# Update your repositories
helm repo update
```

### Installing a Chart

```bash
# Install a chart with default values
helm install my-release lareira/chart-name

# Install with custom values
helm install my-release lareira/chart-name -f values.yaml

# Install with inline value overrides
helm install my-release lareira/chart-name --set key=value
```

## 📦 Available Charts

| Chart | Version | App Version | Description |
|-------|---------|-------------|-------------|
| *Coming Soon* | - | - | Charts will be added as they are developed |

## 🛠 Installation

### From Source

```bash
# Clone the repository
git clone https://github.com/lareira/charts.git
cd charts

# Install a chart from source
helm install my-release ./charts/chart-name
```

### Development Installation

```bash
# Install in development mode with auto-upgrade
helm upgrade --install my-release ./charts/chart-name --debug --dry-run
```

## 👨‍💻 Development

### Creating a New Chart

```bash
# Create a new chart
helm create charts/my-new-chart

# Lint the chart
helm lint charts/my-new-chart

# Test the chart
helm template charts/my-new-chart
```

### Chart Development Guidelines

1. **Follow Helm Best Practices**: Adhere to [Helm chart best practices](https://helm.sh/docs/chart_best_practices/)
2. **Use Semantic Versioning**: Follow [SemVer](https://semver.org/) for chart versions
3. **Document Everything**: Each chart must have comprehensive README.md
4. **Test Thoroughly**: Include unit tests and integration tests where possible
5. **Validate Resources**: Ensure all Kubernetes resources are valid

### Chart Requirements

- Chart.yaml must include proper metadata
- values.yaml must have sensible defaults
- README.md must document all configuration options
- Templates must be well-commented
- Resource limits and requests should be configurable

### Testing

```bash
# Lint all charts
find charts/ -type d -name "Chart.yaml" -execdir helm lint . \;

# Test template rendering
helm template test-release ./charts/chart-name

# Validate against Kubernetes API
helm template test-release ./charts/chart-name | kubectl apply --dry-run=client -f -
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Quick Start for Contributors

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-new-feature`
3. Make your changes following our development guidelines
4. Test your changes thoroughly
5. Commit your changes: `git commit -am 'Add some feature'`
6. Push to the branch: `git push origin feature/my-new-feature`
7. Submit a pull request

### Code Review Process

- All changes require review by a maintainer
- Charts must pass linting and testing
- Documentation must be updated accordingly
- Breaking changes require major version bump

## 📚 Documentation

- [Helm Documentation](https://helm.sh/docs/)
- [Kubernetes Documentation](https://kubernetes.io/docs/)
- [Chart Development Guide](docs/development.md) *(coming soon)*

## 🐛 Support

- **Issues**: [GitHub Issues](https://github.com/lareira/charts/issues)
- **Discussions**: [GitHub Discussions](https://github.com/lareira/charts/discussions)
- **Documentation**: Check individual chart README files

### Reporting Issues

When reporting issues, please include:
- Chart name and version
- Kubernetes version
- Helm version
- Complete error messages
- Steps to reproduce

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🚀 Roadmap

- [ ] Set up automated chart testing
- [ ] Implement chart repository hosting
- [ ] Add security scanning for charts
- [ ] Create comprehensive documentation site
- [ ] Add example applications and use cases

## 📞 Maintainers

- **Lareira Team** - *Initial work* - [Lareira](https://github.com/lareira)

---

⭐ If you find this repository useful, please consider giving it a star!
