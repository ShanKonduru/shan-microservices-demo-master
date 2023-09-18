# Kubernetes CLI (kubectl) Commands

## Cluster Management:

- `kubectl cluster-info`: Display cluster information.
- `kubectl get nodes`: List all nodes in the cluster.
- `kubectl describe node node_name`: Show detailed information about a specific node.

## Pod Management:

- `kubectl get pods`: List all pods in the current namespace.
- `kubectl describe pod pod_name`: Show detailed information about a specific pod.
- `kubectl logs pod_name`: Print the logs of a specific pod.
- `kubectl exec -it pod_name -- container_name command`: Execute a command in a running container within a pod.
- `kubectl delete pod pod_name`: Delete a specific pod.

## Deployment Management:

- `kubectl get deployments`: List all deployments in the current namespace.
- `kubectl describe deployment deployment_name`: Show detailed information about a specific deployment.
- `kubectl scale deployment deployment_name --replicas=3`: Scale the number of replicas for a deployment to 3.
- `kubectl rollout status deployment deployment_name`: Check the status of a deployment rollout.
- `kubectl rollout history deployment deployment_name`: View the revision history of a deployment.
- `kubectl rollout undo deployment deployment_name`: Rollback a deployment to the previous revision.

## Service Management:

- `kubectl get services`: List all services in the current namespace.
- `kubectl describe service service_name`: Show detailed information about a specific service.
- `kubectl expose deployment deployment_name --type=LoadBalancer --port=80`: Expose a deployment as a LoadBalancer service on port 80.
- `kubectl delete service service_name`: Delete a specific service.

## Namespace Management:

- `kubectl get namespaces`: List all namespaces in the cluster.
- `kubectl describe namespace namespace_name`: Show detailed information about a specific namespace.
- `kubectl create namespace namespace_name`: Create a new namespace.
- `kubectl delete namespace namespace_name`: Delete a specific namespace.

## Configuration Management:

- `kubectl create configmap configmap_name --from-file=path/to/file`: Create a ConfigMap from a file.
- `kubectl create secret generic secret_name --from-literal=key=value`: Create a Secret from a literal key-value pair.
- `kubectl describe configmap/configmap_name`: Show detailed information about a specific ConfigMap.
- `kubectl describe secret/secret_name`: Show detailed information about a specific Secret.
- `kubectl get configmaps`: List all ConfigMaps in the current namespace.
- `kubectl get secrets`: List all Secrets in the current namespace.

## Volume Management:

- `kubectl get pv`: List all persistent volumes.
- `kubectl get pvc`: List all persistent volume claims in the current namespace.
- `kubectl describe pv pv_name`: Show detailed information about a specific persistent volume.
- `kubectl describe pvc pvc_name`: Show detailed information about a specific persistent volume claim.

## Health Checks:

- `kubectl get readiness/liveness probe pod_name`: Check the status of readiness or liveness probes for a specific pod.
- `kubectl describe pod pod_name`: Show the status of readiness and liveness probes for containers within a pod.

## Secrets and ConfigMaps:

- `kubectl create secret generic secret_name --from-file=path/to/file`: Create a Secret from a file.
- `kubectl create configmap configmap_name --from-file=path/to/file`: Create a ConfigMap from a file.
- `kubectl create secret generic secret_name --from-literal=key=value`: Create a Secret from a literal key-value pair.
- `kubectl create configmap configmap_name --from-literal=key=value`: Create a ConfigMap from a literal key-value pair.

## Advanced Operations:

- `kubectl apply -f filename`: Apply a configuration file to create or update resources.
- `kubectl explain resource`: Get detailed information about a specific resource.
- `kubectl get events`: List events related to resources in the current namespace.


[![Build Status](https://travis-ci.org/microservices-demo/microservices-demo.svg?branch=master)](https://travis-ci.org/microservices-demo/microservices-demo)

# Sock Shop : A Microservice Demo Application

The application is the user-facing part of an online shop that sells socks. It is intended to aid the demonstration and testing of microservice and cloud native technologies.

It is built using [Spring Boot](http://projects.spring.io/spring-boot/), [Go kit](http://gokit.io) and [Node.js](https://nodejs.org/) and is packaged in Docker containers.

You can read more about the [application design](./internal-docs/design.md).

## Deployment Platforms

The [deploy folder](./deploy/) contains scripts and instructions to provision the application onto your favourite platform. 

Please let us know if there is a platform that you would like to see supported.

## Bugs, Feature Requests and Contributing

We'd love to see community contributions. We like to keep it simple and use Github issues to track bugs and feature requests and pull requests to manage contributions. See the [contribution information](.github/CONTRIBUTING.md) for more information.

## Screenshot

![Sock Shop frontend](https://github.com/microservices-demo/microservices-demo.github.io/raw/master/assets/sockshop-frontend.png)

## Visualizing the application

Use [Weave Scope](http://weave.works/products/weave-scope/) or [Weave Cloud](http://cloud.weave.works/) to visualize the application once it's running in the selected [target platform](./deploy/).

![Sock Shop in Weave Scope](https://github.com/microservices-demo/microservices-demo.github.io/raw/master/assets/sockshop-scope.png)

## 
