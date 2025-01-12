        #Get the documentation for pod manifests
                kubectl explain pods
                
        #Get total nodes in cluster
                kubectl get nodes
                
        #Get pods in current namespace
                kubectl get pods

        #List all namespaces
                kubectl get namespaces
        
        #List contexts added in .kube config
                kubectl config list-contexts
                
        #List the running Pods:
                kubectl get pods
                
        #Select the context to use
                kubectl config use-context <context name>

        #Get the password for the e2e user
                kubectl config view -o jsonpath='{.users[?(@.name == "e2e")].user.password}'

        #Get all pods in all namespaces and list from most resource hungry to less
                kubectl top pod --all-namespaces | sort --reverse --key 3 --numeric | less
                
        #Describe specific pod in deployment that is in the selected namespace with a bit more detail
                kubectl -n <namespace> describe deployments.apps <pod name>
                
        #Delete resources
                kubectl delete

        #Get a deployment's status subresource       
                kubectl get deployment nginx-deployment --subresource=status

        #List all services in the namespace       
                kubectl get services

        #Create temporary curl pod with interactive shell session for troubleshooting
                kubectl run -it --tty --rm curlpod --image=curlimages/curl -- sh -n <namespace>

