# Open Charts Helm Repository

This repository hosts Helm charts and can be added to your Helm repositories.

## Adding the Repository

```bash
helm repo add open-charts https://open-charts.github.io/charts
helm repo update
```

## Installing Charts

```bash
# Install MySQL
helm install my-mysql open-charts/mysql

# Install PostgreSQL
helm install my-postgres open-charts/postgresql

# Install NGINX
helm install my-nginx open-charts/nginx

# Install Redis
helm install my-redis open-charts/redis

# Install RabbitMQ
helm install my-rabbitmq open-charts/rabbitmq
```

## Repository Setup

This repository uses GitHub Pages to host the Helm charts. The charts are automatically published when changes are pushed to the main branch.

### Manual Setup (First Time)

1. Push all the code to GitHub
2. Go to Settings → Actions → General → Workflow permissions
3. Select "Read and write permissions"
4. Check "Allow GitHub Actions to create and approve pull requests"
5. Save the settings
6. Go to Actions tab and run the "Manual Chart Release" workflow
7. Go to Settings → Pages
8. Set Source to "Deploy from a branch"
9. Set Branch to "gh-pages" and folder to "/ (root)"
10. Save

The Helm repository will be available at: https://open-charts.github.io/charts

### Automatic Releases

After the initial setup, any push to the main branch will automatically:
- Package the charts
- Create GitHub releases
- Update the Helm repository index