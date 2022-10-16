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
                
        # Run this project's tests  
                npm test
                
        # Run the script named <foo>
                npm run <foo>
                
        # Search for help on <term> (in a browser)  
                npm help <term>
                
        # Create or verify a user named <username>
                npm login
                         # Options 
                                 --scope = Associate an operation with a scope for a scoped registry
                                 --registry = The base URL of the npm registry
                
        # Log out of the registry
                npm logout
                          # Options 
                                 --scope = Associate an operation with a scope for a scoped registry
                                 --registry = The base URL of the npm registry  
                                
        # Publishes a package to the registry so that it can be installed by name.
                npm publish <package-spec>
                
        # This removes a package version from the registry, deleting its entry and removing the tarball.    
                npm unpublish [<package-spec>]
                
        # Print the folder where npm will install executables.
                npm bin
                
        # This command will print to stdout all the versions of packages that are installed      
                npm ls <package-spec>
                
        # Search the registry for packages matching the search terms
                npm search [search terms ...]
                
        # Print the effective node_modules folder to standard out
                npm root
                
        # Display the npm username of the currently logged-in user
                npm whoami
                
        # This runs a predefined command specified in the "stop" property of a package's "scripts" object.
                npm stop
                
