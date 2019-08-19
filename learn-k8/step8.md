## Test ingress rules

To verify the ingress rules, run the folloing commands to reach to the respective services/deployments/pods

`curl -H "Host: my.kubernetes.example" 172.17.25`{{execute}}
`curl -H "Host: my.kubernetes.example" 172.17.25/hello`{{execute}}
`curl -H "Host: my.kubernetes.example" 172.17.25/HelloFromApp2`{{execute}}