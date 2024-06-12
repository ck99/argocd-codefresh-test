* [How to Model Your GitOps Environments and Promote Releases between Them](https://codefresh.io/blog/how-to-model-your-gitops-environments-and-promote-releases-between-them/)
* [Git Repo](https://github.com/kostis-codefresh/gitops-environment-promotion)

* [How to Structure Your Argo CD Repositories Using Application Sets](https://codefresh.io/blog/how-to-structure-your-argo-cd-repositories-using-application-sets/)
* [Git Repo](https://github.com/kostis-codefresh/many-appsets-demo)


# bootstrap

```
# Create Cluster
kind create cluster

# Bootstrap with ArgoCD
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

# Deploy AppSet
kubectl apply -f k8s/appsets/local-kind-appset.yml
```