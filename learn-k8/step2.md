Now that we have verified the cluster is up and the nodes connected, let's create our first namespace. 

## Creating our first namespace

Check out the pre-loaded YAML file:
`cat ns.yml`{{execute}}

Now, we create the namespace. Run: `kubectl create -f ns.yml`{{execute}}

Verify if the namespace has been created. Execute: `kubectl get namespace`{{execute}}

Now that our namespace has been created, let's move over to creating a deployment and with it k8 pods. Click on **Continue**...
