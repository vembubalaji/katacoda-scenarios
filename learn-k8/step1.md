In this step you will learn how to check the status and the configuration of your k8s cluster.

## Check out the cluster information

First let's ensure cluster is running, for this, run:
`kubectl cluster-info`{{execute}}

Then let's query the K8s API to find out the nodes running in the cluster:
`kubectl get nodes`{{execute}}