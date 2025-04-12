
# K8S Dashboard

### Install

[https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/]

- winget install Helm.Helm
- helm repo add kubernetes-dashboard https://kubernetes.github.io/dashboard/
- helm upgrade --install kubernetes-dashboard kubernetes-dashboard/kubernetes-dashboard --create-namespace --namespace kubernetes-dashboard

### Configure

[https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md]
- kubectl apply -f CreateDashboardServiceAccount.yaml
- kubectl apply -f CreateDashboardClusterRoleBinding.yaml
- kubectl proxy

### Run
- kubectl -n kubernetes-dashboard create token admin-user
- kubectl -n kubernetes-dashboard port-forward svc/kubernetes-dashboard-kong-proxy 8443:443
- [https://localhost:8443/]


