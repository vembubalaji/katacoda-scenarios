In this step you will learn how to check the status and the configuration of your k8s cluster.

## Task

First you need to make sure that your cluster is running, so please run:

`kubectl cluster-info` {{execute HOST1}}

Then you can query the K8s API to find out the nodes running in the cluster:

`kubectl get nodes` {{execute HOST1}}

Then you can look at what is a node, you can see the details of the virtual machine used for the nodes:

The number of CPUs
The amount of memory allocated
The OS running
The resources requested explicitly by the PODs
`kubectl describe node node01` {{execute HOST1}}



We would first create our specific namespace. Check out the pre-loaded YAML file `cat ns.yml` {{execute HOST1}}

Now, we create the namespace `kubectl create -f ns.yml` {{execute HOST1}}

Check how the namespaces have been created, what other namespaces are available `kubectl get namespace` {{execute}}

Now, our namespace has been created. Let's move over to creating a deployment and with it k8 pods. Click on Continue... 

Generated Web Link
https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com

## Markdown

https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com



`sed 's/HOST_IP/[[HOST_IP]]/g' assets\ingress.yml` {{execute}}