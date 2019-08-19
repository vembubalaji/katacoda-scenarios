## Now we have created our first namespace, let's go ahead with our deployments and hence the associated pods. Let's have a look at the yaml file. cat deployment.yml {{execute}}

## Note 1: We have requested for a single replication initially. Let's create the deployment and it's pods.  


## Note 2: We would be deploying it into our newly created namespace. kubectl create -f deployment.yml {{execute}}

## Check how the deployments have been created, Note: we would need to check into the specific namespace (the -n option).  kubectl get deployment -n demoapp {{execute}}

## Now that our deployments are ready, let's expose it to external world and check out the result. Click on Continue...

Generated Web Link
https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com

## Markdown

https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com

kubectl expose deployment hello-world --name=exposed-service --external-ip="[[HOST_IP]]" --port=80 --target-port=80{{execute}}