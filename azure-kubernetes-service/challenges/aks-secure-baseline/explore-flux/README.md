# Explore flux
Increase the replica set for flux and explain behavior. 
- Try scaling the replicas of pod ‘aad-pod-identity-mic’ to 3
    
    kubectl scale --replicas=3 deployment/aad-pod-identity-mic -n cluster-baseline-settings
    
    kubectl get pods -n cluster-baseline-settings
    
    Wait for 2 minutes and then check. The replicas will again come back to 2. Explain why?
