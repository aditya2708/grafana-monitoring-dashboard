# Grafana Monitoring Dashboard

This project sets up a Grafana monitoring dashboard with Prometheus and Node Exporter using Docker.

## Features

- Monitoring of system metrics like CPU, Memory, Disk, and Network using the Node Exporter
- Visualizing metrics in Grafana with pre-configured dashboards
- Alerting system to send notifications when certain thresholds are exceeded

## Prerequisites

- Docker and Docker Compose installed on your system

## Getting Started

1. Clone the repository:

git clone https://github.com/your-username/grafana-monitoring.git

2. Change into the project directory:

cd grafana-monitoring

3. Start the services using Docker Compose:

docker-compose up -d
4. Access the Grafana dashboard at `http://localhost:3000`:
- Username: `admin`
- Password: `admin123` (change this after first login)

5. Explore the pre-configured Node Exporter dashboard to view your system metrics.

## Customization

1. **Alerts**: You can create custom alert rules in Grafana by navigating to the "Alerting" section. Follow the instructions in the [Alerting Guide](alerting-guide.md) to set up alerts for specific metrics.

2. **Dashboards**: You can create your own custom dashboards in Grafana or import additional dashboards from the Grafana community. The dashboard configuration is stored in the `grafana/provisioning/dashboards` directory.

3. **Datasources**: The Prometheus datasource is pre-configured, but you can add additional datasources in the `grafana/provisioning/datasources` directory.

## Maintenance

1. **Backup Grafana Dashboards**: Run the following command to export your Grafana dashboards:

docker-compose exec grafana grafana-cli admin export-dashboards

2. **View Logs**: You can view the logs of the individual services using the following commands:

docker-compose logs grafana
docker-compose logs prometheus
docker-compose logs node-exporter

3. **Update Services**: To update the Docker images, run:

docker-compose pull
docker-compose up -d

## Contributing

If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
