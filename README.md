# k8s-dataplatform-poc

Instructions:

1. Create the kind cluster with the configuration of the file:
`kind create cluster --config kind-config/cluster.yaml`

2. Deploy the boorstrap argoCD:
`k apply -f bootstrap/argocd/bootstrap.yaml`
