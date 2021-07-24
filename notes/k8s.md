# k8s

Kubernetes currently is a graduated CNCF project, which highlights its maturity and reported success from end-user companies. This is because Kubernetes solutionizes portability, scalability, resilience, service discovery, extensibility, and operational cost of containers.

- **Portability**: Kubernetes is a highly portable tool. This is due to its open-source nature and vendor agnosticism. As such, Kubernetes can be hosted on any available infrastructure, including public, private, and hybrid cloud.

- **Scalability**: Building for scale is a cornerstone of any modern infrastructure, enabling an application to scale based on the amount of incoming traffic. Kubernetes has in-build resources, such as HPA (Horizontal Pod Autoscaler), to determine the required amount of replicas for a service. Elasticity is a core feature that is highly automated within Kubernetes.

- **Resilience**: Failure is expected on any platform. However, it is more important to be able to recover from failure fast and build a set of playbooks that minimizes the downtime of an application. Kubernetes uses functionalities like ReplicaSet, readiness, and liveness probes to handle most container failures, enabling powerful self-healing capability.

- **Service Discovery**: it encapsulates the ability to automatically identify and reach new services once these are available. Kubernetes provide cluster level DNS (or Domain Name System), which simplifies the accessibility of workloads within the cluster. Additionally, Kubernetes provides routing and load balancing of incoming traffic, ensuring that all requests are served without application overload.

- **Extensibility**: Kubernetes is a highly extensible mechanism that uses the building-block principle. It has a set of basic resources that can be easily adjusted. Additionally, it provides a rich API interface, that can be extended to accommodate new resources or CRDs (Custom Resource Definitions).

- **Operational Cost**: It refers to the efficiency of resource consumption within a Kubernetes cluster, such as CPU and memory. Kubernetes has a powerful scheduling mechanism that places an application on the node with sufficient resources to ensure the successful execution of the service. As a result, most of the available infrastructure resources are allocated on-demand. Additionally, it is possible to automatically scale the size of the cluster based on the current incoming traffic. This capability is provisioned by the cluster-autoscaler, which guarantees that the cluster size is directly proportional to the traffic that it needs to handle.

## Deploy an application

Kubernetes provides a rich collection of resources that are used to deploy, configure, and manage an application. Some of the widely used resources are:

- Pods - the atomic element within a cluster to manage an application
- Deployments & ReplicaSets - oversees a set of pods for the same application
- Services & Ingress - ensures connectivity and reachability to pods
- Configmaps & Secrets - pass configuration to pods
- Namespaces - provides a logical separation between multiple applications and their resources
- Custom Resource Definition (CRD) - extends Kubernetes API to support custom resources

## Usefull kubectl comands

Kubectl provides a rich set of actions that can be used to interact, manage, and configure Kubernetes resources. Below is a list of handy kubectl commands used in practice.

> Note: In the following commands the following arguments are used:

- RESOURCE is the Kubernetes resource type
- NAME sets the name of the resource
- FLAGS are used to provide extra configuration
- PARAMS are used to provide the required configuration to the resource

### Create Resources

To create resources, use the following command

```kubectl create RESOURCE NAME [FLAGS]```

### Describe Resources

To describe resources, use the following command:

```kubectl describe RESOURCE NAME```

### Get Resources

To get resources, use the following command, where -o yaml instructs that the result should be YAML formated.

```kubectl get RESOURCE NAME [-o yaml]```

### Edit Resources

To edit resources, use the following command, where -o yaml instructs that the edit should be YAML formated.

```kubectl edit RESOURCE NAME [-o yaml]```

### Label Resources

To label resources, use the following command:

```kubectl label RESOURCE NAME [PARAMS]```

### Port-forward to Resources

To access resources through port-forward, use the following command:

```kubectl port-forward RESOURCE/NAME [PARAMS]```

### Logs from Resources

To access logs from a resource, use the following command:

```kubectl logs RESOURCE/NAME [FLAGS]```

### Delete Resources

To delete resources, use the following command:

```kubectl delete RESOURCE NAME```
