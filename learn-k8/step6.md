## Ingress

## Create Deployment

To start, we deploy an example java apps that will be the target of our requests. 
The deployment contains three deployments, one called webapp1 and a second called webapp2, and a third called webapp3 with a service for each.

Create deployments:
`kubectl create -f ingress/ingress-deployment.yml`{{execute}}

Create services:
`kubectl create -f ingress/ingress-service.yml`{{execute}}