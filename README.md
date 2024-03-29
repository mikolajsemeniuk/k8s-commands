# K8S commands

Set of kubectl commands

## Nodes

### Get nodes
* `kubectl get nodes`

## Context

### Get contexts

* `kubectl config get-contexts`

### Show current context

* `kubectl config current-context`

### Use context

* `kubectl config use-context {context}`

## Namespaces

### Get all namespaces

* `kubectl get namespaces`
* `kubectl get ns`

### Set default namespace

* `kubectl config set-context --current -n {namespace}`
* `kubectl config set-context --current --namespace={namespace}`

## Pods

### Get pods in current namespace

* `kubectl get po`
* `kubectl get pods`

### Create pod from file
* `kubectl apply -f {pod.yaml}`

### Describe pod

* `kubectl describe po {pod_id}`

### Show pod environment variables

* `kubectl exec -it {pod_id} -- env`

### Show pod logs

* `kubectl logs {pod_id}`

## Services

### Get services
* `kubectl get services`
* `kubectl get svc`

## Deployments

### Get deployments
* `kubectl get deployments`
* `kubectl get deploy`

## Replicasets

### Get replicasets
* `kubectl get replicasets`
* `kubectl get rs`

## Configmap

### Show configmap

* `kubectl describe cm {pod_id}`
* `kubectl describe configmap {pod_id}`

### Edit configmap

* `kubectl edit {configmap}`

## Port-Forward

### Forward to local port:
* `kubectl port-forward pod/{pod_id} 8080:80`
