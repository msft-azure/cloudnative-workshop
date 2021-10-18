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
 - [NGINX](https://www.nginx.com/products/nginx-ingress-controller)
 - [AGIC](https://docs.microsoft.com/en-us/azure/application-gateway/ingress-controller-overview)
 - [Contour](https://github.com/projectcontour/contour)
 - [HAProxy](https://www.haproxy.org/)
 - [Traefic](https://github.com/traefik/traefik)

#### Network firewalls
- [WAF](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-network#secure-traffic-with-a-web-application-firewall-waf)
- [Azure Firewall](https://docs.microsoft.com/en-us/azure/firewall/protect-azure-kubernetes-service)
- [Kubernetes network policies](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-network#control-traffic-flow-with-network-policies)

## Authentication and Authorisation

## Azure Security Centre Integration

## Azure Policies

## Container registry and image security

## Opertions
### Monitoring
- Container Insights
- Prometheus integration
- Application Insights
#### Service Mesh
