# Kokoaly Private Docker Registry

Kokoaly Private Docker Registry allows you to deploy docker registry to AWS EKS. Integrated with ALB, SSM Parameter Store and S3.

## Prerequisites
* Amazon EKS as a Kubernetes cluster service.
* Amazon S3 as a Docker Registry object storage.
* Amazon Route53 or similar used as DNS service.
* Amazon ACM to manage the renewal and deployment of public certificates used with ACM-integrated Elastic Load Balancing service.
* [AWS Load Balancer Controller](https://kubernetes-sigs.github.io/aws-load-balancer-controller/v2.2/) deployed on a EKS cluster.
* [Kubernetes External Secrets](htts://github.com/external-secrets/kubernetes-external-secrets) deployed on a EKS cluster.

## Installing the Helm Chart
To install the chart with the release named kokoaly-docker-register:
```bash
$ helm install kokoaly-docker-registry kokoaly-docker-registry
```

## Uninstalling the Chart
To uninstall/delete the deployment:
```bash
$ helm delete kokoaly-docker-registry
```

## Future enchancements
* LucidChart diagram of the deployed service
* Use Kubernetes service account
* Static code analysis [Checkov](https://github.com/bridgecrewio/checkov)
* HA solution for Redis using Kubernetes or integrate with [Amazon ElastiCache for Redis](https://aws.amazon.com/redis)
* Refactor Helm chart without static configurations
* Proper authentication to private Docker Registry
* Example Terraform to deploy underlying infrastructure

    
