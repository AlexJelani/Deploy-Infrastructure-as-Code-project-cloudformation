# CD12352 - Infrastructure as Code Project Solution
# [Jelani Alexander]

## Spin up instructions
# CD12352 - Infrastructure as Code Project Solution

# Infrastructure Deployment Guide

## Preview instructions

* Preview the network stack:
```
./infrastructure.sh preview us-east-1 udagram-network network.yml network-parameters.json
```
* Preview the application stack:
```
./infrastructure.sh preview us-east-1 udagram-app udagram.yml udagram-parameters.json
```



## Spin up instructions

* Deploy the network stack:
```
./infrastructure.sh deploy us-east-1 udagram-network network.yml network-parameters.json
```
* Deploy the application stack:
  
```
./infrastructure.sh deploy us-east-1 udagram-app udagram.yml udagram-parameters.json
```
  
## Tear down instructions
* Delete the application stack:

```
./infrastructure.sh delete us-east-1 udagram-app
```
* Delete the network stack:
```
./infrastructure.sh delete us-east-1 udagram-network
``` 
## Other considerations
* The infrastructure uses high availability design with resources across multiple AZs
* Auto Scaling Group maintains 4 servers in private subnets
* S3 bucket automatically empties before stack deletion
* Health checks are configured for the Load Balancer
* All resources are properly tagged for cost tracking  
