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
                
        # create resource(s)
                kubectl apply -f ./my-manifest.yaml
        
        # create from multiple files
                kubectl apply -f ./my1.yaml -f ./my2.yaml
                
        # create resource(s) in all manifest files in dir
                kubectl apply -f ./dir
                
        # create resource(s) from url
                kubectl apply -f https://git.io/vPieo

        # start a single instance of nginx
                kubectl create deployment nginx --image=nginx
                
        # create a Job which prints "Hello World"
                kubectl create job hello --image=busybox:1.28 -- echo "Hello World"
                
        # create a CronJob that prints "Hello World" every minute
                kubectl create cronjob hello --image=busybox:1.28   --schedule="*/1 * * * *" -- echo "Hello World"        
