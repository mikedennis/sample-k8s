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
- ClusterIP (internal), Ingress (external-L7) vs LoadBalancer (external-L4)