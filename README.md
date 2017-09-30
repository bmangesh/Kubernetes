# Kubernetes

Kubernetes is an open-source platform for automating deployment, scaling, and operations of application containers across clusters of hosts, providing container-centric infrastructure.

It has many features which are especially useful for applications running in production, like service naming and discovery, load balancing, application health checking, horizontal auto-scaling, and rolling updates.

Components of k8s:

Pod – This is the basic unit in Kubernetes. It can consist of one or more containers that are guaranteed to be co-located on the host machine and share the same resources. All containers deployed inside pod can see other containers via localhost. Each pod has a unique IP address within the cluster

Service – This is a set of pods that work together. By default, a service is exposed inside a cluster but it can also be exposed onto an external  IP address outside your cluster. We can expose it using one of four available behaviors: ClusterIP, NodePort, LoadBalancer and ExternalName.

Replication Controller – This is a specific type of Kubernetes controller. It handles replication and scaling by running a specified number of copies of a pod across the cluster. It is also responsible for pod replacement if the underlying node fails.

Key concepts of Kubernetes:

Kubernetes is an open source orchestration system for Docker containers. It manages containerized applications across multiple hosts and provides basic mechanisms for deployment, maintenance, and scaling of applications.

It allows the user to provide declarative primitives for the desired state, for example “need 5 apache servers and 1 MySQL server running”. Kubernetes self-healing mechanisms, such as auto-restarting, re-scheduling, and replicating containers then ensure this state is met. The user just define the state and Kubernetes ensures that the state is met at all times on the cluster.


Product
Description
kube-apiserver
Configure and validate objects like Pod or Services (definition of access to services in container) through REST API 
kube-scheduler
Allocate Pods to each node
kube-controller-manager
Execute Status management, manage replication controller
kubelet
Run on each node as agent and manage Pod
calico
Enable inter-Pod connection using BGP
kube-proxy
Configure iptable NAT tables to configure IP and load balance (ClusterIP)
etcd
Distribute KVS to store Kubernetes and Calico information
etcd-proxy
Run on each node and transfer client request to etcd clusters





Future improvements and questions:
Use environmental variables for configuration rather than hard coding in the docker files
Find a better way to manage logging/monitoring (graphite container?)
Find a better way to startup and restart pods
Find a way to force nodes to retrieve the latest version of the image from a repository (currently its caching and not checking for updates)
Fully script building the cluster
How to do rolling updates
How to manage database updates/migrations/backups



