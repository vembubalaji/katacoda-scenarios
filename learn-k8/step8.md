## Test ingress rules

To verify the ingress rules, run the folloing commands to reach to the respective services/deployments/pods

`curl -H "Host: my.kubernetes.example" [[HOST_IP]]`{{execute}}
`curl -H "Host: my.kubernetes.example" [[HOST_IP]]/hello`{{execute}}
`curl -H "Host: my.kubernetes.example" [[HOST_IP]]/HelloFromApp2`{{execute}}