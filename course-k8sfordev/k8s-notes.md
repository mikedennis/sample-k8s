# k8s-notes

### Course and Samples
[https://github.com/DanWahlin/DockerAndKubernetesCourseCode]
- kubetctl apply -f myyaml.yml --save-config

### Pods
- /DockerAndKubernetesCourseCode/samples/pods/nginx.pod.yml
- kubectl port-forward my-nginx 8080:80
- [http://localhost:8080]

### Deployments
- /DockerAndKubernetesCourseCode/samples/deployments
- kubectl port-forward pod/my-nginx-xxxx 8080:80
- kubectl port-forward deployment/my-nginx 8080:80
- kubectl get deployment --show-labels
- kubectl scale deployment my-nginx --replicas=5
- Rolling update (default), blue-green, canary

### Services
- /DockerAndKubernetesCourseCode/samples/services
- Layer 4 load balancer
- ClusterIP, NodePort, LoadBalancer, ExternalName (maps DNS)
- ClusterIP (internal), Ingress (external-L7) vs LoadBalancer (external-L4) [https://medium.com/google-cloud/kubernetes-nodeport-vs-loadbalancer-vs-ingress-when-should-i-use-what-922f010849e0]

### Volumes
- emptyDir, hostPath, azureDisk, azureFile, elasticBlockStore
- [https://github.com/kubernetes/examples]

### ConfigMap
- config via environment vars or access as file via a volume
- options --from-file, --from-env-file, --from-literal
- can load env from entire configmap - configMapRef: -name: app-settings

### Secrets
- can encode tls secret: --cert= --key=
- secrets are only base64 encoded in manifest

