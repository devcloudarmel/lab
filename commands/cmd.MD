Basic Commands

    kubectl version
    
    kubectl cluster-info

    kubectl get nodes
    
    kubectl describe node [node-name]

Pod Management

    kubectl get pods    
        All pods in the current namespaces

    kubectl get pods -n [namespace]
        All pods in the specified namespace

    kubectl describe pod [pod-name]

    kubectl logs [pod-name]

    kubectl exec -it [pod-name] -- [command]
        Executes a command inside a running pod.

    kubectl delete pod [pod-name]
        Deletes a specific pod.

Service Management

    kubectl get svc
        Lists all services in the current namespace.

    kubectl describe svc [service-name]
        Provides detailed information about a specific service.

    kubectl expose [resource] --port=[port] --target-port=[target-port]
        Exposes a resource (e.g., pod, deployment) as a new Kubernetes service.

Deployment Management

    kubectl get deployments
        Lists all deployments in the current namespace.

    kubectl describe deployment [deployment-name]
        Provides detailed information about a specific deployment.

    kubectl create deployment [deployment-name] --image=[image]
        Creates a new deployment with the specified name and image.

    kubectl set image deployment/[deployment-name] [container-name]=[new-image]
        Updates the image of a container in a deployment.

    kubectl rollout status deployment/[deployment-name]
        Checks the rollout status of a deployment.

    kubectl delete deployment [deployment-name]
        Deletes a specific deployment.

Namespace Management

    kubectl get namespaces
        Lists all namespaces in the cluster.

    kubectl create namespace [namespace-name]
        Creates a new namespace.

    kubectl delete namespace [namespace-name]
        Deletes a specific namespace.

    kubectl config set-context --current --namespace=[namespace]
        Set namespace

ConfigMaps and Secrets

    kubectl create configmap [configmap-name] --from-literal=[key]=[value]
        Creates a ConfigMap from literal key-value pairs.

    kubectl get configmaps
        Lists all ConfigMaps in the current namespace.

    kubectl describe configmap [configmap-name]
        Provides detailed information about a specific ConfigMap.

    kubectl create secret generic [secret-name] --from-literal=[key]=[value]
        Creates a generic secret from literal key-value pairs.

    kubectl get secrets
        Lists all secrets in the current namespace.

    kubectl describe secret [secret-name]
        Provides detailed information about a specific secret.

Resource Quotas and Limits

    kubectl get resourcequotas
        Lists all resource quotas in the current namespace.

    kubectl describe resourcequota [quota-name]
        Provides detailed information about a specific resource quota.

    kubectl get limits
        Lists all resource limits in the current namespace.

    kubectl describe limitrange [limitrange-name]
        Provides detailed information about a specific limit range.

Role-Based Access Control (RBAC)

    kubectl get roles
        Lists all roles in the current namespace.

    kubectl get rolebindings
        Lists all role bindings in the current namespace.

    kubectl describe role [role-name]
        Provides detailed information about a specific role.

    kubectl describe rolebinding [rolebinding-name]
        Provides detailed information about a specific role binding.

Persistent Volumes and Claims

    kubectl get pv
        Lists all persistent volumes in the cluster.

    kubectl describe pv [pv-name]
        Provides detailed information about a specific persistent volume.

    kubectl get pvc
        Lists all persistent volume claims in the current namespace.

    kubectl describe pvc [pvc-name]
        Provides detailed information about a specific persistent volume claim.
