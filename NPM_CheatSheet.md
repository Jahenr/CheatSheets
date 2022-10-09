NPM / Node Package Manager

        # To install all the packages defined in package.json
                npm install 

        # To install a particular package for the given project
                npm install package_name

        # To install a particular package for all the projects, in other words install package with global scope
                npm install package_name -g

        # To Lists the installed versions of all dependencies in this software
                npm list
        
        # Remove packages globally
                npm uninstall -g package-name        
    
        # Show global packages    
                npm list -g
        
        # List all npm configuration flags
                npm config ls -l
        
        # Update the global npm version.
                npm update npm -g
     
        # Locally edit a dependency
                npm edit <module_name>
       
        # Test & Show the full dependency tree 
                npm install --dry-run
