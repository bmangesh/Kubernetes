# Kubernetes

Kubernetes is an open-source platform for automating deployment, scaling, and operations of application containers across clusters of hosts, providing container-centric infrastructure.

It has many features which are especially useful for applications running in production, like service naming and discovery, load balancing, application health checking, horizontal auto-scaling, and rolling updates.

Components of k8s:

Pod – This is the basic unit in Kubernetes. It can consist of one or more containers that are guaranteed to be co-located on the host machine and share the same resources. All containers deployed inside pod can see other containers via localhost. Each pod has a unique IP address within the cluster

Service – This is a set of pods that work together. By default, a service is exposed inside a cluster but it can also be exposed onto an external  IP address outside your cluster. We can expose it using one of four available behaviors: ClusterIP, NodePort, LoadBalancer and ExternalName.

Replication Controller – This is a specific type of Kubernetes controller. It handles replication and scaling by running a specified number of copies of a pod across the cluster. It is also responsible for pod replacement if the underlying node fails.
