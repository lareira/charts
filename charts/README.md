# Charts Directory

This directory contains all the Helm charts provided by this repository.

## Directory Structure

Each chart should follow this structure:

```
chart-name/
├── Chart.yaml          # Chart metadata
├── values.yaml         # Default configuration values
├── templates/          # Kubernetes manifest templates
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── ingress.yaml
│   ├── configmap.yaml
│   ├── _helpers.tpl    # Template helpers
│   └── NOTES.txt       # Installation notes
├── tests/             # Chart tests (optional)
├── crds/              # Custom Resource Definitions (if needed)
└── README.md          # Chart documentation
```

## Adding a New Chart

1. Create a new directory with your chart name
2. Use `helm create charts/your-chart-name` as a starting point
3. Customize the templates and values for your application
4. Update Chart.yaml with proper metadata
5. Write comprehensive documentation in README.md
6. Test thoroughly before submitting

## Chart Guidelines

- Follow semantic versioning
- Include resource limits and requests
- Make configurations configurable via values.yaml
- Include proper labels and annotations
- Document all configuration options