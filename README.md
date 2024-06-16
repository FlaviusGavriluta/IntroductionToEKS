# Introduction to EKS

## Story

You decided to move your cluster to the cloud. You're thinking about choosing a cloud provider, so you decide on trying out AWS EKS.

## What are you going to learn?

- How to create a kubernetes cluster in AWS
- How to use the kubectl CLI
- How to scale up an EKS cluster

## Tasks

1. Create a new VPC called `my-vpc` with CIDR 10.0.0.0/16
    - A new VPC called `my-vpc` with CIDR 10.0.0.0/16 is created.

2. Create EKS on the AWS Console, or with ```eksctl``` with the latest version of k8s.
    - Kubectl, aws-cli downloaded, and installed on your computer

3. Create a Deployment in your cluster with cli, with an ubuntu alpine image on it, then get some information about about the running deployments on your cluster.
    - The deployment is shown on the cluster and is in a running state.

4. Check the events of the deployment. Scale up the number of pods of the deployment to a minimum number of 6.
    - The events of the deployment are shown.
    - There are six pods inside the deployment.

5. Add another node to the cluster.
    - You can see on the AWS Console that one more node is added.

6. Delete the deployment.
    - Whenever checking the cluster, the deployment is not found.

## General requirements

None

## Hints

- How to get kubecontext 
  ``` aws eks --region <AWS_REGION> update-kubeconfig --name <EKS_NAME> --profile <AWS_ROFILE> ```
- How to set cubecontext
  ``` kubectl config set-context <EKS_ARN> ```
- You should only set kubecontext once per cluster.
- When you scale something, be patient. It takes some time to upscale or downscale cluster resources.

## Background materials

- <i class="far fa-book-open"></i> [Getting started with Amazon EKS](https://aws.amazon.com/eks/getting-started/)
- <i class="far fa-exclamation"></i> [AWS EKS - Create Kubernetes cluster on Amazon EKS](https://www.youtube.com/watch?v=p6xDCz00TxU)
- <i class="far fa-exclamation"></i> [kubectl command reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands)
- <i class="far fa-exclamation"></i> [Getting started with eksctl - AWS](https://docs.aws.amazon.com/eks/latest/userguide/getting-started-eksctl.html)
- <i class="far fa-exclamation"></i> [eksctl command reference](https://eksctl.io/introduction/#getting-started)
