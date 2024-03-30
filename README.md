# K8S commands

Set of kubectl commands

## All
`kubectl get all`

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

## Replication controller

### Get replication controllers
* `kubectl get replicationcontrollers`
* `kubectl get rc`

### Scale replication controller
* `kubectl scale --replicas=6 rc/{replication controller name}`
* `kubectl scale --replicas=6 replicationcontrollers/{replication controller name}`

## Replicasets

### Get replicasets
* `kubectl get replicasets`
* `kubectl get rs`

### Scale replicaset
* `kubectl scale --replicas=6 rs/{replica name}`
* `kubectl scale --replicas=6 replicaset/{replica name}`

## Deployments

### Get deployments
* `kubectl get deployments`
* `kubectl get deploy`

### Update image of deployment
* `kubectl set image deployment/{deployment name} nginx=nginx:1.9.1`

### Check last deployment status (how pods were created and destroyed)
* `kubectl rollout status deploy/deploy`

### Check history of all revisions in given deployment
* `kubectl rollout history deploy/deploy`

### Rollback latest version
* `kubectl rollout undo deploy/deploy`

### Rollback to given revision
* `kubectl rollout undo deployment/deploy --to-revision=2`

## Services

### Get services
* `kubectl get services`
* `kubectl get svc`

## Configmap

### Show configmap

* `kubectl describe cm {pod_id}`
* `kubectl describe configmap {pod_id}`

### Edit configmap

* `kubectl edit {configmap}`

## Port-Forward

### Forward to local port:
* `kubectl port-forward pod/{pod_id} 8080:80`
