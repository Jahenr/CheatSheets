NPM / Node Package Manager

        # Initialize a node.js project
                npm init
                        # Options 
                                -y = Skip all questions and use default values

        # Install all packages defined in package.json
                npm install 

        # Install a particular package for the given project
                npm install package_name

        # Install a particular package for all projects, in other words install package with global scope
                npm install package_name -g

        # Install a package as a development dependency
                npm install package_name --save-dev

        # To Lists the installed versions of all dependencies in this software
                npm list
                
        # To Update production packages
                npm update

        # Remove a package from the project
                npm uninstall package_name

        % To Lists the latest versions of all dependencies in this software
                npm view
                
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
                
        # Show npm version
                npm --version
                
        # Scan and list all the vulnerabilities in the project
                npm audit
