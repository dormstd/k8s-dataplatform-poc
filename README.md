# k8s-dataplatform-poc

Instructions:

1. Create the kind cluster with the configuration of the file:
`kind create cluster --config kind-config/cluster.yaml`

2. Deploy the kind version of ingress-nginx:
`k kustomize manifests/platform-infra/ingress-nginx | k apply -f -`

3. Run:
`k kustomize argocd | k apply --server-side --force-conflicts -f -`

4. Deploy the applications to argoCD:
`k kustomize argocd-resources/platform-infra | k apply -f -`
