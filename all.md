choco
choco install minikube
cls
minikube
minikube start --vm-driver=hyperv
minikube delete
wsl
wsl -l -v
wsl --update
wsl
wsl --update --pre-release
wsl
wsl --shutdown
wsl
wsl -l -v
wslconfig /l
wsl --update --pre-release
wsl --update
lhp
wsl.exe -t Ubuntu
wsl --list --online
wsl --install -d Ubuntu-20.04
wsl
choco install kubernetes-cli
kubectl version --client
cd ~
mkdir .kube
cd .kube
New-Item config -type file
kubectl cluster-info
kubectl cluster-info dump
choco install --force kubernetes-cli
cls
kubectl cluster-info
kubectl cluster-info dump
cls
kubectl version --client
cls
New-Item -Path 'c:\' -Name 'minikube' -ItemType Directory -Force
Invoke-WebRequest -OutFile 'c:\minikube\minikube.exe' -Uri 'https://github.com/kubernetes/minikube/releases/latest/download/minikube-windows-amd64.exe' -UseBasicParsing
$oldPath = [Environment]::GetEnvironmentVariable('Path', [EnvironmentVariableTarget]::Machine)`
if ($oldPath.Split(';') -inotcontains 'C:\minikube'){`
  [Environment]::SetEnvironmentVariable('Path', $('{0};C:\minikube' -f $oldPath), [EnvironmentVariableTarget]::Machine)`
}`

minikube start
lhp
wsl --shutdown
wsl --update
wsl
wsl -l -v
minikube start
kubectl cluster-info dump
kubectl cluster-info
cls
kubectl get pods -A
minikube dashboard
minikube addons enable metrics-server
cls
kubectl get pods -A
minikube delete --all
minikube start --driver=hyperv
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-Management-PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-Tools-All
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-All
Install-WindowsFeature -Name Hyper-V, RSAT-Hyper-V-Tools
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-Tools-All -All
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-All
minikube start --driver=hyperv
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-Tools-All -All
Get-WindowsOptionalFeatures
Get-WindowsOptionalFeature
Get-WindowsOptionalFeature -Online -FeatureName _hyper-v_ | select DisplayName, FeatureName
cls
minikube start
cls
minikube start --driver=docker
minikube delete --all
cls
minikube start
minikube status
kubectl get nodes
kubectl create deployment hello-minikube --image=kicbase/echo-server:1.0
kubectl get deployments
kubectl expose deployment hello-minikube --type=NodePort --port=8080
minikube service hello-minikube --url
kubectl delete deployment hello-minikube
kubectl delete services hello-minikube
kubectl get pods
cls
kubectl run nginx --image=nginx
kubectl get pods
kubectl escribe pod nginx
kubectl describe pod nginx
kubectl get pods
cls
kubectl get pods -o wide
kubectl delete pods --all
cls
kubectl get pods
cls
notepad pod-definition.yaml
type .\pod-definition.yaml
kubectl apply -f .\pod-definition.yaml
kubectl get pods
kubectl describe pod nginx-pod
cls
kubectl delete pods --all
kubectl apply -f .\pod-definition.yaml
kubectl apply -f .\nginx.yaml
kubectl get pods
kubectl apply -f .\nginx.yaml
kubectl get pods
cls
kubectl delete pods --all
cls
kubectl create -f .\rc-definition.yaml
kubectl get replicationcontroller
kubectl get rc
kubectl get pods
kubectl delete rc
kubectl delete rc myapp-rc
cls
kubectl get pods
kubectl create -f .\rs-definition.yaml
cls
kubectl create -f .\rs-definition.yaml
kubectl get replicasets
kubectl get replicaset
kubectl get rs
kubectl replace -f .\rs-definition.yaml
kubectl scale --replicas=6 -f .\rs-definition.yaml
kubectl scale --replicas=2 rs myapp-rs
kubectl get rs
kubectl delete rs --all
cls
cd rs
kubectl create -f .\replicaset.yaml
kubectl get po
kubectl delete pod myapp-replicaset-66zkr
kubectl get po
cls
kubectl delete pods --all
kubectl get po
kubectl describe replicaset myapp-replicaset
cls
kubectl get po
cd ..\pods\
kubectl create -f .\nginx.yaml
kubectl get po
kubectl describe replicaset myapp-replicaset
cls
kubectl get all
kubectl delete rs myapp-replicaset
cls
kubectl get all
kubectl create -f .\deployment.yaml
kubectl get deploy
cls
kubectl get rs
kubectl get po
kubectl rollout status deployment.apps/myapp-deployment
kubectl get deploy
kubectl delete deploy --all
kubectl rollout status deployment.apps/myapp-deployment
kubectl create -f .\deployment.yaml
kubectl rollout status deployment.apps/myapp-deployment
kubectl rollout history deployment.apps/myapp-deployment
kubectl delete deploy --all
kubectl create -f .\deployment.yaml --record
kubectl rollout history deployment.apps/myapp-deployment
kubectl edit deployment myapp-deploymen
kubectl edit deployment myapp-deployment
kubectl rollout history deployment.apps/myapp-deployment
kubectl rollout status deployment.apps/myapp-deployment
cls
kubectl get deploy
kubectl delete deploy --all
kubectl create -f .\deployment.yaml
kubectl set image deployment myapp-deployment nginx=nginx:1.18-perl --record
kubectl rollout history deployment.apps/myapp-deployment
kubectl rollout status deployment.apps/myapp-deployment
kubectl get pods
cls
kubectl edit deployment myapp-deployment
kubectl rollout status deployment.apps/myapp-deployment
kubectl get pods
kubectl rollout undo deployment.apps/myapp-deployment
kubectl rollout status deployment.apps/myapp-deployment
kubectl get service
minikube ip
kubectl port-forward service/myapp-service 30008:80
minikube service myapp-service --url