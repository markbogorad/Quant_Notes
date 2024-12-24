up:: [[Computer Science MOC]]
tags:: #Programming  
# Kubernetes
- Another [[Containerization Tools]]
- Kubernetes takes containerization a step further by providing a robust platform for automating the deployment, scaling, and management of these containers in a cluster.
#### Key Concepts in Kubernetes:
1. **Cluster**:
    - A Kubernetes cluster is a set of nodes (physical or virtual machines) that run containerized applications. The cluster is managed by the Kubernetes control plane.
2. **Node**:
    - A node is a worker machine in a Kubernetes cluster. Each node runs containerized applications and is managed by the control plane.
3. **Pod**:
    - A pod is the smallest deployable unit in Kubernetes. It represents a single instance of a running process in the cluster and can contain one or more containers that share resources.
4. **Deployment**:
    - A deployment is a Kubernetes resource that defines how to deploy and manage a set of identical pods. It ensures that the desired number of pod replicas are running at all times.
5. **Service**:
    - A service is a Kubernetes resource that defines a logical set of pods and a policy for accessing them. It provides load balancing and service discovery for the pods.
6. **Namespace**:
    - A namespace is a way to divide cluster resources between multiple users or teams. It provides a scope for names to avoid naming conflicts.

## Basic Commands
- **Create a Deployment**:
	- `kubectl create deployment myapp --image=myimage`
- **Expose a Deployment**:
	- `kubectl expose deployment myapp --type=LoadBalancer --port=80`
- **Scale a Deployment**:
	- `kubectl scale deployment myapp --replicas=3`
- **Get Pods**:
	- `kubectl get pods`
- **Delete a Deployment**:
	- `kubectl delete deployment myapp`
