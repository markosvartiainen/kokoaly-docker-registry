# Kokoaly Private Docker Registry

Kokoaly Private Docker Registry allows you to use docker registry in AWS EKS. Integrated with ALB, SSM Parameter Store and S3.

## Prerequisites
* Amazon EKS as a Kubernetes cluster service.
* Amazon S3 as a Docker Registry object storage.
* Amazon ACM to manage the renewal and deployment of public certificates used with ACM-integrated Elastic Load Balancing service.
* [AWS Load Balancer Controller](https://kubernetes-sigs.github.io/aws-load-balancer-controller/v2.2/) deployed on a EKS cluster.
* [Kubernetes External Secrets](htts://github.com/external-secrets/kubernetes-external-secrets) deployed on a EKS cluster.
  

