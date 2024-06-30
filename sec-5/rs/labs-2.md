`kubectl get po` : Lists all pods in the current namespace.

`kubectl get rs` : Lists all ReplicaSets in the current namespace.

`kubectl describe rs new-replica-set` : Describes detailed information about the ReplicaSet named "new-replica-set".

`kubectl get pods` : Lists all pods in the current namespace.

`kubectl delete pod new-replica-set-jnzln` : Deletes the pod named "new-replica-set-jnzln".

`vim replicaset-definition-1.yaml` : Opens the file "replicaset-definition-1.yaml" for editing using Vim.

`kubectl create -f /root/replicaset-definition-1.yaml` : Creates a ReplicaSet using the configuration in "replicaset-definition-1.yaml".

`vim replicaset-definition-2.yaml` : Opens the file "replicaset-definition-2.yaml" for editing using Vim.

`kubectl create -f /root/replicaset-definition-2.yaml` : Creates a ReplicaSet using the configuration in "replicaset-definition-2.yaml".

`kubectl get rs` : Lists all ReplicaSets in the current namespace.

`kubectl delete rs replicaset-1` : Deletes the ReplicaSet named "replicaset-1".

`kubectl delete -f replicaset-definition-2.yaml` : Deletes the ReplicaSet defined in "replicaset-definition-2.yaml".

`kubectl edit replicaset new-replica-set` : Opens the ReplicaSet named "new-replica-set" for editing.

`kubectl get pods --all` : Lists all pods in the current namespace, including those in various states.

`kubectl delete pods --all` : Deletes all pods in the current namespace.

`kubectl get pods` : Lists all pods in the current namespace.

`kubectl scale rs new-replica-set --replicas=5` : Scales the ReplicaSet named "new-replica-set" to 5 replicas.

`kubectl replace -f /path/to/updated-replicaset-definition.yaml` : Replaces an existing ReplicaSet with the updated configuration from the specified YAML file.

`kubectl delete pods -l name=busybox-pod` : Deletes pods with the label `name=busybox-pod`.

`history | awk '{ $1=""; print }'` : Lists command history with timestamps, removing the first column.
