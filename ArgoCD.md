Before this you need to set up a cluster with minikube or any other provider and configure kubectl

1. Install argocd  
        `kubectl create namespace argocd`  
        `kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml`
2. Access the argocd API server with cli
    1. Install argocd-cli (windows)  
        `choco install argocd-cli`
3. Access the web UI
    1. Kubectl port-forwarding  
        `kubectl port-forward svc/argocd-server -n argocd 8080:443`
    2. Get the admin password
        `argocd admin initial-password -n argocd`
    3. Visit <http://localhost:8080/> and login with user admin and the password you just got

If you want to add a different cluster:  
1. First get you clusters from kubectl  
    `kubectl config get-contexts -o name`
2. Add them to argocd 
    `argocd cluster add <your contextname>`


