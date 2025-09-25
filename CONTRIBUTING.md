# Contributing to Lareira Helm Charts

Thank you for your interest in contributing to our Helm charts repository! This document provides guidelines and information about contributing to this project.

## Code of Conduct

By participating in this project, you are expected to uphold our Code of Conduct. Please report unacceptable behavior to the maintainers.

## How to Contribute

### Reporting Issues

- Use the GitHub issue tracker to report bugs or request features
- Check existing issues before creating a new one
- Provide clear reproduction steps for bugs
- Include relevant versions (Helm, Kubernetes, chart version)

### Submitting Changes

1. **Fork** the repository
2. **Create** a feature branch from `main`
3. **Make** your changes following our guidelines
4. **Test** your changes thoroughly
5. **Submit** a pull request

## Development Guidelines

### Chart Standards

- Follow [Helm best practices](https://helm.sh/docs/chart_best_practices/)
- Use semantic versioning for charts
- Include comprehensive documentation
- Ensure backward compatibility when possible

### Code Style

- Use 2 spaces for indentation in YAML files
- Keep lines under 120 characters
- Use meaningful variable names
- Comment complex template logic

### Testing Requirements

- Lint charts with `helm lint`
- Test template rendering with `helm template`
- Validate against Kubernetes API
- Include unit tests where applicable

## Review Process

- All PRs require maintainer review
- Changes must pass CI/CD checks
- Breaking changes require major version bump
- Documentation must be updated

## Questions?

Feel free to open an issue or start a discussion if you have questions!