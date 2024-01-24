1. Install argocd  
        `kubectl create namespace argocd`  
        `kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml`
2. Access the argocd API server with cli
    1. Install argocd-cli (windows)  
        `choco install argocd-cli`
    2. 
3. Access the web UI
    1. Kubectl port-forwarding  
        `kubectl port-forward svc/argocd-server -n argocd 8080:443`
    2. Visit <http://localhost:8080/>

