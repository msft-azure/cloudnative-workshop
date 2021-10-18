# Azure Kubernetes Service Best Practices

## AKS Architecture
- [AKS Secure Baseline](https://github.com/mspnp/aks-secure-baseline)
- [Enterprise scale Landing zone](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/aks/enterprise-scale-landing-zone)

## Security

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

## Authentication and Authorisation
- [Azure AD-Kubernetes RBAC](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-identity#use-kubernetes-role-based-access-control-kubernetes-rbac)
- [Azure AD-Azure RBAC](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-identity#use-azure-rbac)
- [Azure AD-Pod-managed Identities](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-identity#use-pod-managed-identities)

## Azure Security Centre Integration
- [Defender for Kubernetes](https://docs.microsoft.com/en-us/azure/security-center/defender-for-kubernetes-introduction)
- [Protect Kubernetes workload](https://docs.microsoft.com/en-us/azure/security-center/kubernetes-workload-protections#availability)

## Azure Policies
- [Azure Policy Regulatory Compliance for AKS](https://docs.microsoft.com/en-us/azure/aks/security-controls-policy)

## Container registry and image security
- [Secure Images](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-container-image-management)
- [Defender for Container Registries](https://docs.microsoft.com/en-us/azure/security-center/defender-for-container-registries-introduction)
- [Scan Registry images](https://docs.microsoft.com/en-us/azure/security-center/defender-for-container-registries-usage)
- [Scan images in CI/CD pipeline](https://docs.microsoft.com/en-us/azure/security-center/defender-for-container-registries-cicd)

## Cluster Security
- [Cluster Security](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-cluster-security)

## Operations
### Monitoring
- Container Insights
- Prometheus integration
- Application Insights
#### Service Mesh
