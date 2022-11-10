# Example extracted from:
https://medium.com/style-theory-engineering/infrastructure-as-code-kubernetes-a2f050389f26 and
https://kubernetes.io/docs/tutorials/hello-minikube/ and
https://www.digitalocean.com/community/tutorials/how-to-use-minikube-for-local-kubernetes-development-and-testing
https://github.com/GoogleCloudPlatform/kubernetes-engine-samples/tree/main/hello-app


# Install minikube
https://minikube.sigs.k8s.io/docs/start/

# Install e.g. docker
https://docs.docker.com/get-docker/

# Get image into minikube:
```
docker pull <imagename>
minikube image load <imagename>
```

# Sync minikube with docker:
`eval $(minikube docker-env)`

# Start minikube:
`minikube start`

# Deploy the yaml file:
`kubectl apply -f hello.yaml`

# Delete deployment
`kubectl delete deployment hello-world-deployment`

# See deployments

# Get url from loadbalancer
`minikube service hello-world-lb --url`

# Kill pod:
FInd pod via: `kubectl get pods`
Kill pod via: `kubectl delete pod <podname>`
See that it was killed by `kubectl get events`

