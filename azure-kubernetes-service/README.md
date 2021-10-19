# Azure Kubernetes Service - Well Acrhitected - Best Practices

## AKS Architecture
- [AKS Secure Baseline](https://github.com/mspnp/aks-secure-baseline)
- [Enterprise scale Landing zone](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/aks/enterprise-scale-landing-zone)

## 1. Security

### Networking
####  KubeNetworking Model
 - [Azure CNI Networking](https://docs.microsoft.com/en-us/azure/aks/configure-kubenet)
 - [Kubenet networking](https://docs.microsoft.com/en-us/azure/aks/configure-azure-cni)

#### AKS Service options
[Service types details](https://docs.microsoft.com/en-us/azure/aks/concepts-network#services)
- ClusterIP
- LoadBalancer
- NodePort
- ExternalName

#### Ingress Controllers
Ingress cotrollers available:
 - [NGINX](https://www.nginx.com/products/nginx-ingress-controller)
 - [AGIC](https://docs.microsoft.com/en-us/azure/application-gateway/ingress-controller-overview)
 - [Contour](https://github.com/projectcontour/contour)
 - [HAProxy](https://www.haproxy.org/)
 - [Traefic](https://github.com/traefik/traefik)

#### Network firewalls
- [WAF](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-network#secure-traffic-with-a-web-application-firewall-waf)
- [Azure Firewall](https://docs.microsoft.com/en-us/azure/firewall/protect-azure-kubernetes-service)
- [Kubernetes network policies](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-network#control-traffic-flow-with-network-policies)
- [Bastion host to AKS nodes](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-network#securely-connect-to-nodes-through-a-bastion-host)

### Authentication and Authorisation
- [Azure AD-Kubernetes RBAC](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-identity#use-kubernetes-role-based-access-control-kubernetes-rbac)
- [Azure AD-Azure RBAC](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-identity#use-azure-rbac)
- [Azure AD-Pod-managed Identities](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-identity#use-pod-managed-identities)

### Azure Security Centre Integration
- [Defender for Kubernetes](https://docs.microsoft.com/en-us/azure/security-center/defender-for-kubernetes-introduction)
- [Protect Kubernetes workload](https://docs.microsoft.com/en-us/azure/security-center/kubernetes-workload-protections#availability)

### Azure Policies
- [Azure Policy Regulatory Compliance for AKS](https://docs.microsoft.com/en-us/azure/aks/security-controls-policy)

### Container registry and image security
- [Secure Images](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-container-image-management)
- [Defender for Container Registries](https://docs.microsoft.com/en-us/azure/security-center/defender-for-container-registries-introduction)
- [Scan Registry images](https://docs.microsoft.com/en-us/azure/security-center/defender-for-container-registries-usage)
- [Scan images in CI/CD pipeline](https://docs.microsoft.com/en-us/azure/security-center/defender-for-container-registries-cicd)

### Cluster Security
- [Cluster Security](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-cluster-security)
- [Pod Security Policy](https://docs.microsoft.com/en-us/azure/aks/use-pod-security-policies)
- [Key Vault- Secret store driver](https://docs.microsoft.com/en-us/azure/aks/developer-best-practices-pod-security#limit-credential-exposure) 
- AKS automatically updates security patches, [Kured](https://github.com/weaveworks/kured) for reboot
- [API server-Private AKS cluster](https://docs.microsoft.com/en-us/azure/aks/private-clusters)
- [API server using authorized IP](https://docs.microsoft.com/en-us/azure/aks/api-server-authorized-ip-ranges)


## 2. Operations
### Cluster Isolation
- [Physically isolate clusters](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-cluster-isolation#physically-isolate-clusters)
- [Logically isolate clusters with namespaces](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-cluster-isolation#logically-isolate-clusters)
### Isolation Dimensions
- Scheduling
  -  [Taints and Tolerations](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-advanced-scheduler#provide-dedicated-nodes-using-taints-and-tolerations)- hard constraints
  -  [Node Selectors and affinity](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-advanced-scheduler#control-pod-scheduling-using-node-selectors-and-affinity)- soft constraints
- Networking
  - [Kubernetes network policies](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-network#control-traffic-flow-with-network-policies)
- Authentication and Authorisation
  - RBAC with AAD
- Containers

### Resource Management 
- [Resource Quotas](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-scheduler#enforce-resource-quotas) 
- [Limit Range](https://kubernetes.io/docs/tasks/administer-cluster/manage-resources/memory-default-namespace)
- [Pod Disruption Budget](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-scheduler#plan-for-availability-using-pod-disruption-budgets)

### Monitoring
- [Azure Monitor Container Insights](https://docs.microsoft.com/en-us/azure/aks/monitor-aks)
- [Prometheus integration](https://docs.microsoft.com/en-us/azure/azure-monitor/containers/container-insights-prometheus-integration)
- [Application Insights] (https://docs.microsoft.com/en-us/azure/azure-monitor/app/kubernetes-codeless)

### DevOps
- [CI/CD to AKS with GitHub Actions](https://docs.microsoft.com/en-us/azure/developer/jenkins/deploy-from-github-to-aks)
- [CI/CD to AKS with Azure DevOps](https://docs.microsoft.com/en-us/azure/devops-project/azure-devops-project-aks?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Faks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json)

### Service Mesh
- [Selection Criteria](https://docs.microsoft.com/en-us/azure/aks/servicemesh-about#selection-criteria)
- [Istio](https://istio.io/latest/docs/setup/install/)
- [Linkerd](https://linkerd.io/2.11/getting-started/)
- [Consul Connect](https://learn.hashicorp.com/tutorials/consul/service-mesh-deploy)

### Storage
- [Storage options](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-storage)
  - Azure Files
  - Azure Disks
  - Blobfuse

## 3. Perfromance
### Scaling
- [Manually scale](https://docs.microsoft.com/en-us/azure/aks/concepts-scale#manually-scale-pods-or-nodes)
- [Horizontal pod autoscaler (HPA)](https://docs.microsoft.com/en-us/azure/aks/concepts-scale#horizontal-pod-autoscaler)
- [Cluster autoscaler](https://docs.microsoft.com/en-us/azure/aks/concepts-scale#cluster-autoscaler)
- [Burst to Azure Container Instances](https://docs.microsoft.com/en-us/azure/aks/concepts-scale#burst-to-azure-container-instances)

## 4. Reliability
- [AKS Availability zones](https://docs.microsoft.com/en-us/azure/aks/availability-zones)
- [Azure paired regions](https://docs.microsoft.com/en-us/azure/best-practices-availability-paired-regions) 
- [Geo replication for Container images](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-multi-region#enable-geo-replication-for-container-images)
- [Storage Migration plan](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-multi-region#create-a-storage-migration-plan)

## 5. Cost Management
- [Cost Saving options for Nodes](https://azure.microsoft.com/en-in/pricing/details/kubernetes-service/)
  -  [1 year reserved]
  -  [3 years reserved]
  -  [spot instance]
- [multiple nodes and enable scale to zero](https://docs.microsoft.com/en-us/learn/modules/aks-optimize-compute-costs/2-node-pools)
- [AKS resource-quota policies by using Azure Policy](https://docs.microsoft.com/en-us/learn/modules/aks-optimize-compute-costs/6-resource-quota-azure-policy)
