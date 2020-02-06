+++
title = "Networking"
date = 2018-12-09T17:00:54-05:00
weight = 500

+++

## [Networking](https://kubernetes.io/docs/concepts/cluster-administration/networking/)

#### Highly-coupled container-to-container communications

#### Pod-to-Pod communications

#### Pod-to-Service communications

#### External-to-Service communications

##### 1. NodePort(Not recommended)

It opens a specific port on all the Cluster Nodes, and any traffic that is sent to this port is forwarded to the service.

##### 2. LoadBalancer

A Kubernetes LoadBalancer service points to external load balancers that are NOT in the Kubernetes cluster, but exist elsewhere. For AWS, it uses ELB and GKE it uses Network Load Balancer.

Downside of this is that each service you expose with a LoadBalancer will get its own IP address, and you have to pay for a LoadBalancer per exposed service, which can get expensive!

##### 3. Ingress

Ingress is NOT a type of service. Instead, it sits in front of multiple services and act as a "smart router" or entrypoint into your cluster.

##### 4. Api Gateway

Everything that you get from Ingress plus below points: 

* Authentication & Authorization for users / 3rd-party systems
* Enforce SLAs for different users / 3rd-party systems
* Data transformation / translation
* API lifecycle management
* Rate limiting
* Billing
* Other customized requirements ….
