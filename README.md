# Schedule App Helm Chart Repository
This repository contains Helm charts for deploying the backend and frontend components of the Schedule app on Kubernetes clusters.

## Source Code Repositories

- [Frontend Source Code Repository](https://github.com/stratiiv/schedule-frontend)
- [Backend Source Code Repository](https://github.com/DTG-cisco/devops-team-green-2)

## Charts

#### Prerequisites

- Kubernetes cluster
- Helm installed ([Helm Installation Guide](https://helm.sh/docs/intro/install/))
- "app" namespace and "pg-user-pass" secrets in Kubernetes cluster
```bash
kubectl create namespace app
kubectl create secret generic pg-user-pass --from-literal=username=<your_username> --from-literal=password=<your_password> -n app
```

### Backend Chart

#### Installation

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/stratiiv/schedule-app-charts.git
    cd schedule-app-charts
    ```

2. **Install the Backend chart:**

    ```bash
    helm install <release-name> backend
    ```

### Frontend Chart

#### Installation

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/stratiiv/schedule-app-charts.git
    cd schedule-app-charts
    ```

2. **Install the Frontend chart:**

    ```bash
    helm install <release-name> frontend
    ```
    
#### Configuration
Customize your deployment by replacing values in the values.yaml file in each chart

