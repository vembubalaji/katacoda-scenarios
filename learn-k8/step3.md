Now we have created our first namespace, let's go ahead with our deployments and the associated pods. 

## Creating our deployment

Let's have a look at the yaml file. `cat deployment.yml`{{execute}}

- Note 1: We have requested for a single replication initially.
- Note 2: We would be deploying it into our newly created namespace. 

To create the deployment, execute: `kubectl create -f deployment.yml`{{execute}}

Check the deployments that we have created just now;  `kubectl get deployment -n demoapp`{{execute}}
- Note: we would need to check into the specific namespace (the -n option).

Also, check the associated pods. Run: `kubectl get pods -n demoapp`{{execute}}

A complete description of the deployment is also possible. This would give us a snapshot of the deployment.

`kubectl describe deployment demoapp-deployment -n demoapp`{{execute}}

Now that our deployments and PODS are ready, let's check out how to create services and expose it's IP. Click on **Continue**...