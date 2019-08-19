Now that we have the deployments and services ready, let's create an ingress deployment and service.
The YAML file ingress.yaml defines a Nginx-based Ingress controller together with a service making it available on Port 80 to external connections using ExternalIPs. 

To update the host ip in the YAML file, run the below command:
`sed -i 's/HOST_IP/[[HOST_IP]]/g' ingress/ingress.yml`{{execute}}

To create an ingress deployment and its' service, run the below command:
`kubectl create -f ingress/ingress.yml`{{execute}}

To check the status of ingress deployment and other details, run the below command
`kubectl get deployment -n nginx-ingress`{{execute}}

We have the ingress server running, now, we need to configure the routes. Check the file ingress-rules.yml. `cat ingress/ingress-rules.yml`{{execute}}

`kubectl create -f ingress/ingress-rules.yml`{{execute}}

The rules apply to requests for the host my.kubernetes.example.

Once the ingress deployment is done, we can get the rules by running the below command;
`kubectl get ing`{{execute}}