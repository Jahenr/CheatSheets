        #Get total nodes in cluster
                kubectl get nodes
                
        #Get pods in current namespace
                kubectl get pods

        #List all namespaces
                kubectl get namespaces
        
        #List contexts added in .kube config
                kubectl config list-contexts
                
        #Select the context to use
                kubectl config use-context <context name>

        #Get all pods in all namespaces and list from most resource hungry to less
                kubectl top pod --all-namespaces | sort --reverse --key 3 --numeric | less
                
        #Describe specific pod in deployment that is in the selected namespace with a bit more detail
                kubectl -n <namespace> describe deployments.apps <pod name>
                
