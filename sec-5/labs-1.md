`kubectl get po` : Lists all pods in the current namespace.

`k run --image nginx` : Creates a new deployment named "nginx" using the nginx image.

`k run nginx --image nginx` : _Deprecated:_ Creates a new deployment named "nginx" using the nginx image.

`k run nginx --image=nginx` : Creates a new deployment named "nginx" using the nginx image with correct syntax.

`k delete po --all` : Deletes all pods in the current namespace.

`k run nginx --image=nginx` : Creates a new deployment named "nginx" using the nginx image.

`k get pods` : Lists all pods in the current namespace.

`k describe pod newpods-fxmbf` : Describes detailed information about the pod named "newpods-fxmbf".

`kubectl get pods -o wide` : Lists pods with additional details like node and IP information.

`kubectl get pods` : Lists all pods in the current namespace.

`kubectl describe pods webapp` : Describes detailed information about the pod named "webapp".

`kubectl get pod webapp -o jsonpath='{.spec.containers[*].name}'` : Retrieves names of containers in the pod "webapp".

`kubectl get pod webapp -o jsonpath='{.spec.containers[*].name}' | wc -w` : Counts the number of containers in the pod "webapp".

`kubectl get pod webapp -o jsonpath='{range .spec.containers[*]}{.name}: {.image}{"\n"}{end}'` : Lists names and images of containers in the pod "webapp".

`kubectl get pod webapp -o jsonpath='{.status.containerStatuses[?(@.name=="agentx")].state}'` : Retrieves the state of the container "agentx" in the pod "webapp".

`k delete pod webapp` : Deletes the pod named "webapp".

`kubectl run redis --image=redis123 --dry-run=client -o yaml` : Simulates creating a pod named "redis" with the image "redis123" in YAML format without actually creating it.

`k edit pod redis` : Opens the pod definition of "redis" in the default editor for editing.

`kubectl apply -f redis-definition.yaml` : Applies the configuration in "redis-definition.yaml" to create or update Kubernetes resources.

`history | awk '{ $1=""; print }'` : Lists command history with timestamps, removing the first column.
