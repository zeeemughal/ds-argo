# ds-argo

bootstrap k8s cluster

# create secret for cloudflare api token
kubectl create secret generic cloudflare-api-token \
  --namespace cert-manager \
  --from-literal=api-token=<tokenhere>                                                                                                                                                 
# port-forward with kubectl
kubectl port-forward svc/argocd-server -n argocd 8080:443
# get argo secret
kubectl get secret argocd-initial-admin-secret -n argocd -o jsonpath="{.data.password}" | base64 -d
