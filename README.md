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
* Configure Kubernetes Service Accounts, roles and role bindings. 
* Enable [IAM Roles for Service Accounts](https://docs.aws.amazon.com/eks/latest/userguide/iam-roles-for-service-accounts.html)
* Enable [OPA Gatekeeper](https://github.com/open-policy-agent/gatekeeper) or similar for Kubernetes policy management.
* Stateful HA solution for Redis using Kubernetes or integrate with [Amazon ElastiCache for Redis](https://aws.amazon.com/redis)
* Refactor Helm chart without static configurations
* Example Terraform to deploy underlying infrastructure
* [Docker Registry Token Authentication](https://docs.docker.com/registry/spec/auth/)
* AWS CloudFront as CDN
* Manage EKS deployments with ArgoCD in GitOps way.
* Enable [Horizontal Pod Autoscaling](https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/)
* Enable [EKS logging with fluentd-bit](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Container-Insights-setup-logs-FluentBit.html)

    
