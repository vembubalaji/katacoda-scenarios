## Ingress

#### Create Deployment

To start, we deploy an example java app that will be the target of our requests. 
The deployment descriptor contains three deployments, one called *webapp1* and a second called *webapp2*, and a third called *webapp3* with a service for each.

Check out the **ingress/ingress-deployment.yml** and **ingress/ingress-service.yml** files.

Create deployments:
`kubectl create -f ingress/ingress-deployment.yml`{{execute}}

Create services:
`kubectl create -f ingress/ingress-service.yml`{{execute}}