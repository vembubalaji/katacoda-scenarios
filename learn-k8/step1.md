In this step you will learn how to check the status and the configuration of your k8s cluster.

## Task

This creates:
`echo "Run in Terminal"`{{execute}}

First you need to make sure that your cluster is running, so please run:
`kubectl cluster-info`{{execute}}

Then you can query the K8s API to find out the nodes running in the cluster:
`kubectl get nodes`{{execute}}


We would first create our specific namespace. Check out the pre-loaded YAML file:
`cat ns.yml`{{execute}}

Now, we create the namespace `kubectl create -f ns.yml`{{execute}}

Check how the namespaces have been created, what other namespaces are available `kubectl get namespace`{{execute}}

Now, our namespace has been created. Let's move over to creating a deployment and with it k8 pods. Click on Continue... 

Generated Web Link
https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com

## Markdown

https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com



`sed 's/HOST_IP/[[HOST_IP]]/g' assets\ingress.yml`{{execute}}