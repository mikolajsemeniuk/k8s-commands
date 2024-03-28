# K8S commands

Set of kubectl commands

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

### Set default namespace

* `kubectl config set-context --current --namespace={namespace}`

## Pods

### Get pods in current namespace

* `kubectl get po`
* `kubectl get pods`

### Get pods in selected namespace

* `kubectl get po -n {namespace}`
* `kubectl get pods -n {namespace}`

### Show pod environment variables

* `kubectl exec -it {pod_id} -- env`

### Show pod logs

* `kubectl logs {pod_id}`

## Configmap

### Show configmap

* `kubectl describe cm {pod_id}`
* `kubectl describe configmap {pod_id}`

### Edit configmap

* `kubectl edit {configmap}`
