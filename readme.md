Installing Kubernetes Cluster with 3 minions on CentOS 7 to manage pods and services
====================================================================================

From  http://severalnines.com/blog/installing-kubernetes-cluster-minions-centos7-manage-pods-services

This is to provide a simple base for creating a Kubbernetes cluster on your local
machine.

Stating up Cluster
------------------

The following will start the full Cluster

```vagrant up```

Machine names are master, minion1, minion2, minion3

As of now - the master script is NOT idempotent.

Still todo:

Add instructions on deploying a container on the cluster.
links to some tutorials to get things going.
