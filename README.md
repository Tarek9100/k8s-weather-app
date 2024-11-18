# Kubernetes Weather App

This is a Kubernetes-based weather application, forked and enhanced from the original project created by [Ahmed El Fakharany](https://github.com/abohmeed/k8s-course-lab). The application demonstrates modern Kubernetes practices and showcases a weather service, authentication, and a frontend UI.

## Project Overview

The weather app is deployed using Kubernetes and includes the following services:
- **Authentication Service**: Handles user management and authentication.
- **Weather Service**: Provides weather information using a third-party API.
- **Frontend UI**: A user-friendly interface for interacting with the app.

### Architecture
The project uses:
- **MySQL**: Database for authentication service.
- **Kubernetes**: For container orchestration.
- **Nginx Ingress**: For managing external access to the services.
- **Secrets and ConfigMaps**: For managing sensitive and configuration data.

## Setup and Deployment

### Prerequisites
- Kubernetes cluster (e.g., Kind, Minikube, or a cloud provider)
- kubectl installed and configured
- Docker (for building images if necessary)

### Steps to Deploy the Application
1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/k8s-weather-app.git
   cd k8s-weather-app
2. **Create a Kind Cluster with Ingress Use the provided cluster configuration:**
   kind create cluster --config=kind-config.yaml
3. **Apply Kubernetes Manifests Deploy services, deployments, and ingress:**
   kubectl apply -f kubernetes/
4. **Update /etc/hosts Add the following entry to your hosts file:**
   <your-cluster-ip> weatherapp.local
5. **Access the Application:**
   Open http://weatherapp.local in your browser.
