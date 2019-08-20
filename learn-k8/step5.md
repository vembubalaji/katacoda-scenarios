Now that we have seen how to deploy and create services for a container, let's see how to scale them up or down;

## Scaling up and Scaling down

If we need to increase the number of deployments for a particular deployment and hence it's corresponding pods, then we can run the following command;

`kubectl scale deployment demoapp-deployment --replicas=5 -n demoapp`{{execute}}

Here we are increasing the replicas to five.

Let's check the deployment and the pods now.

`kubectl get deployment -n demoapp`{{execute}}

`kubectl get pods -n demoapp`{{execute}}

Check out the number of pods active.

To descale, just reduce the replicas
`kubectl scale deployment demoapp-deployment --replicas=2 -n demoapp`{{execute}}

Now if we run the pods status;
`kubectl get deployment -n demoapp`{{execute}}
`kubectl get pods -n demoapp`{{execute}}

We would see few pods status as terminating, and after a few seconds, the pods would be removed from the namespace with only two effictive pods.
`kubectl get deployment -n demoapp`{{execute}}
`kubectl get pods -n demoapp`{{execute}}