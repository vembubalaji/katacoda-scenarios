We have till now seen how to create a namespace and how to create pods and deployments. Now we would create a service and expose it's IP to the external world.

## Creating Services

Let's have a look at the yaml file. `cat service.yml`{{execute}}
Note: We would need to update the host_ip in the yaml file with the host's IP address. For this, run the following command. 

`sed -i 's/HOST_IP/[[HOST_IP]]/g' service.yml`{{execute}}

Once this is done, create the service. Execute the below command;

`kubectl create -f service.yml`{{execute}} 
This would create the service for the deployments. Check for the service and the exposed ip using the below command;

`kubectl get svc -n demoapp`{{execute}}

Finally let's give a call to the deployed service.

`curl http://[[HOST_IP]]:8080/hello`{{execute}}

Let's tail the logs..

`kubectl -n demoapp logs -f deployment/demoapp-deployment --all-containers=true`{{execute}}

And run the curl from the second host.

`curl http://[[HOST_IP]]:8080/hello`{{execute HOST2}}
