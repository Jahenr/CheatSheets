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
       # get the password for the e2e user
                kubectl config view -o jsonpath='{.users[?(@.name == "e2e")].user.password}'
