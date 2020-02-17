+++
title = "Networking"
date = 2018-12-09T17:00:54-05:00
weight = 500

+++

## [Networking](https://kubernetes.io/docs/concepts/cluster-administration/networking/)

Kubernetes dictates the following requirements on any networking implementation: 

* All Pods can communicate with all other Pods without using network address translation (NAT).
* All Nodes can communicate with all Pods without NAT.
* The IP that a Pod sees itself as is the same IP that others see it as.

##### Four distinct Network problems to address: 

1. Highly-coupled container-to-container communications

2. Pod-to-Pod communications

3. Pod-to-Service communications

4. External-to-Service communications
