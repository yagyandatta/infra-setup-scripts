# Monitoring and Alerting Setup

This script sets up a monitoring and alerting system using Prometheus and Grafana.

## Prerequisites

- A Debian-based, Arch-based, or RHEL-based operating system
- Sudo privileges

## What the Script Does

1. Detects the operating system type (Debian, Arch, or RHEL)
2. Updates the package manager
3. Installs Git if not already present
4. Installs Docker if not already present
5. Installs Docker Compose if not already present
6. Clones the Prometheus-Grafana monitoring and alerting repository
7. Starts the services using Docker Compose
8. Verifies that the services are running correctly

## Usage

To use this script, navigate to the monitoring_alerting directory and run:

```bash
./setup.sh
```

## Services

This setup includes the following services:

- Prometheus: A monitoring system and time series database
- Grafana: A platform for monitoring and observability

## Access URLs

After successful setup, you can access the services at:

- Prometheus: `http://localhost:9100` or `http://<your-ip>:9100`
- Grafana: `http://localhost:3000` or `http://<your-ip>:3000`

## Troubleshooting

- To check the logs of all services: `docker-compose logs -f`
- To view logs of a specific container: `docker logs <container_id>`

## Note

This script will remove any existing `prometheus-grafana-monitoring-alerting` directory in the current path before cloning a fresh copy of the repository.

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/yagyandatta/infra-setup-scripts/blob/main/LICENSE) file for details.
