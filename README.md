# Helm Chart for CVE Processor Web Application

This Helm chart deploys the CVE Processor web application along with its PostgreSQL database.

## Prerequisites

- Kubernetes cluster (e.g., Minikube, Kind)
- Helm 3.x
- Docker

## Installation

1. Clone the repository:
    ```
    git clone https://github.com/cyse7125-su24-team15/helm-webapp-cve-processor.git
    ```

2. Clone the repository:
    ```
    cd helm-webapp-cve-processor/csye7125
    ```

3. Install the Helm chart:
    ```
    helm install csye7125 .
    ```

This will deploy the CVE Processor web application and its PostgreSQL database in the `csye7125` namespace.

## Configuration

The following table lists the configurable parameters of the CVE Processor chart and their default values.

| Parameter                 | Description                                    | Default                           |
|---------------------------|------------------------------------------------|-----------------------------------|
| `replicaCount`            | Number of replicas for the web app and database| 1                                 |
| `namespace`               | Namespace to deploy the application            | csye7125                          |
| `app.image`               | Image repository for the web application       | chlokesh1306/cve-processor        |
| `app.tag`                 | Image tag for the web application              | 1.1.0                             |
| `postgres.image`          | Image repository for PostgreSQL                | postgres                          |
| `postgres.tag`            | Image tag for PostgreSQL                       | latest                            |
| `initContainer.image`     | Image repository for the database migration job| chlokesh1306/database-migration   |
| `initContainer.tag`       | Image tag for the database migration job       | 1.0.1                             |

You can override the default values by providing a YAML file with custom values using the `--values` flag during installation.

## Uninstallation

To uninstall the CVE Processor chart, run the following command:
    ```
    helm uninstall csye7125
    ```

This will remove all the Kubernetes resources associated with the chart.

## Contributing

Please follow the standard GitHub workflow:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with descriptive messages.
4. Push your changes to your forked repository.
5. Submit a pull request to the main repository.

Please ensure that your code follows the existing style and conventions used in the project.