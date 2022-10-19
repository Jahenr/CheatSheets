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
                
        # To show the NPM Version Command
                npm version

        # To manage the ownership of the published package
                npm owner
        
        # NPM Build Command: It is used to build a package
                npm build

        # Manage package owners  
                npm owner

        # Start a script defined in package.json file eg. npm run client, npm run server
                npm run <script name>

        # Set access level on published packages 
                npm access

        # Add a registry user account
                npm adduser

        # Run a security audit
                npm audit

        # Display npm bin folder
                npm bin

        # Bugs for a package in a web browser
                npm bugs

        # Manipulates packages cache
                npm cache

        # Install a project with a clean slate
                npm ci

        # Tab completion for npm
                npm completion

        # Reduce duplication
                npm dedupe

        # Deprecate a version of a package
                npm deprecate

        # The registry diff command
                npm diff

        # Docs for a package in a web browser maybe
                npm docs

        # Modify package distribution tags
                npm dist-tag

        # Check your environments
                npm doctor

        # Run a command from an npm package
                npm exec

        # Explain installed packages
                npm explain

        # Browse an installed package
                npm explore

        # Find duplication in the package tree
                npm find-dupes

        # Retrieve funding information
                npm fund

        # Search npm help documentation
                npm help

        # Get help on npm via search
                npm help-search

        # Manage registry hooks
                npm hook

        # Create a package.json file
                npm init

        # Symlink a package folder
                npm link

        # Log out of the registry
                npm logout

        # Manage orgs
                npm org

        # Check for outdated packages
                npm outdated

        # Manage package owners
                npm owner

        # Ping npm registry
                npm ping

        # Manage your package.json
                npm pkg

        # Change settings on your registry profile
                npm profile

        # Remove extraneous packages
                npm prune

        # Publish a package
                npm publish

        # Retrieve a filtered list of packages
                npm query

        # Rebuild a package
                npm rebuild

        # Open package repository page in the browser
                npm repo

        # Restart a package
                npm restart

        # Display npm root folder
                npm root

        # Run arbitrary package scripts
                npm run-script

        # Lock down dependency versions for publication
                npm shrinkwrap

        # Mark your favorite packages
                npm star

        # View packages marked as favorites
                npm stars

        # Start a package
                npm start

        # Stop a package
                npm stop

        # Manage organization teams and team memberships
                npm team

        # Test a package
                npm test

        # Manage your authentication tokens
                npm token

        # Remove a package from the registry
                npm unpublish

        # Remove an item from your favorite packages
                npm unstar

        # Update a package
                npm update

        # View registry info
                npm view

        # Display npm username
                npm whoami

        # Run a command from an npm package
                npx
                
        # Show npm version
                npm --version
                
        # Check for outdated packages
                npm outdated     

        # Scan and list all the vulnerabilities in the project
                npm audit

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
                