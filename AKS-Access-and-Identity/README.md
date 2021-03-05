# AKS Authorization and Authentication

## References

### Use Azure role-based access controls to define access to the Kubernetes configuration file in Azure Kubernetes Service (AKS)

https://docs.microsoft.com/bs-latn-ba/azure/aks/control-kubeconfig-access

### A Primer on Kubernetes Access Control

https://thenewstack.io/a-primer-on-kubernetes-access-control/

# Generate kubeconfig (get-credentials)

## References

### az aks get-credentials

https://docs.microsoft.com/en-us/cli/azure/aks?view=azure-cli-latest#az-aks-get-credentials

## Examples

Generate kubeconfig file for admins.

```
az aks get-credentials \
  --subscription REPLACE-WITH-YOUR-SUBSCRIPTION \
  --resource-group REPLACE-WITH-YOUR-AKS-RG \
  --name REPLACE-WITH-YOUR-AKS-NAME \
  --file ./REPLACE-WITH-YOUR-FILE-NAME.kubeconfig \
  --admin
```

Generate kubeconfig file for users.

```
az aks get-credentials \
  --subscription REPLACE-WITH-YOUR-SUBSCRIPTION \
  --resource-group REPLACE-WITH-YOUR-AKS-RG \
  --name REPLACE-WITH-YOUR-AKS-NAME \
  --file ./REPLACE-WITH-YOUR-FILE-NAME.kubeconfig
```

# Admin vs User - Security concerns

## References

### Regular user with RBAC enabled cluster has system:masters role

https://github.com/Azure/AKS/issues/1343#issuecomment-615908008

### az aks get-credentials should return unique credentials for each user instead of returning shared credentials

https://github.com/Azure/AKS/issues/397