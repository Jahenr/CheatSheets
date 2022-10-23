# Dart

   CheatSheet

      # install Dart on a Windows using Chocolatey
      It requires administrator privileges.
         `choco install dart-sdk`
      

      # install Dart on a Linux Machine
         - `sudo apt-get update`
         - `sudo apt-get install dart`


      # install Dart on a Mac with Homebrew
         - `brew tap dart-lang/dart`
         - `brew install dart`
      

      # check Dart SDK version on your local computer
         `dart --version`


      # create a new Dart project the default way with all dependencies
         `dart create <APP_NAME>`
      

      # create a new Dart project based on a template
         `dart create -t TEMPLATE_NAME <APP_NAME>`


      # create a new project and don't load project dependencies
         `dart create --no-pub <APP_NAME>`


      # create a new project if the same project already exist in that path
         `dart create --force <DIRECTORY>`


      # run a Dart project
         - `cd <APP_NAME>`
         - `dart run`


      # run tests for a project
         `dart test`


      # compile project for production and to various formats.
         `dart compile exe bin/file_name_where_main_is.dart`

      
      # enable Dart Lang analytics
         `dart --enable-analytics`

      
      # disable Dart Lang analytics
         `dart --disable-analytics`

      
      #  show additional command output.
         `dart --verbose`


      # analyze Dart code in a directory.
         `dart analyze`


      # open DevTools (optionally connecting to an existing application).
         `dart devtools`

      
      # prints the DevTools version.
         `dart devtools --version`

      
      # output more informational messages.
         `dart devtools --verbose`


      # hostname to serve DevTools on (defaults to localhost).
         `dart devtools --host=<host>`


      #  port to serve DevTools on; specify 0 to automatically use any available port. (defaults to "9100")
         `dart devtools --port=<port>`


      #  launches DevTools in a browser immediately at start. (defaults to on unless in --machine mode)
         `dart devtools --launch-browser`

      
      # sets output format to JSON for consumption in tools.
         `dart devtools --machine`

      
      # generate API documentation for Dart projects
         `dart doc`

      
      #  configure the output directory for doc
         `dart doc -o <DIRECTORY>`
      
      
      #  display warnings for broken links.
         `dart doc --validate-links`
      
      
      # try to generate the docs without saving them.
         `dar doc --dry-run`

      
      # apply automated fixes to Dart source code.  
         `dart fix`
      
      
      #  preview the proposed changes but make no changes.
         `dart fix --dry-run`
      
      
      # apply the proposed changes.
         `dart fix --apply`

      
      #  idiomatically format Dart source code to fit accepted rules
         `dart format`

      
      # perform null safety migration on a project.
         `dart migrate`
      
      
      # apply the proposed null safety changes to the files on disk.
         `dart migrate --apply-changes`

     
      #  attempt to perform null safety analysis even if the project has analysis errors.
         `dart migrate  --ignore-errors`

      
      #  go ahead with migration even if some imported files have not yet been migrated.
         `dart migrate --skip-import-check`
      
     
      # add a third-party package
         `dart pub add <NAME_OF_PACKAGE>`

      
      # work with system cache
         `dart pub cache`

      
      # downgrade the current package's dependencies to oldest versions
         `dart pub downgrade`
      
      
      # log into pub.dev
         `dart pub login`
      
      
      # log out pub.dev
         `dart pub logout`
      
      
      # analyze your dependencies to find which ones can be upgraded
         `dart pub outdated`
      
      
      # publish the current package to pub.dartlang.org
         `dart pub publish`
      
      
      # removes a dependency from the current package
         `dart pub remove <NAME_OF_PACKAGE>`

      
      #  upgrade the current package's dependencies to latest versions
         `dart pub upgrade`
      
      
      # get a third-party package dependencies into your project
         `dart pub get <NAME_OF_PACKAGE>`
      
      # for further information on any command-line options
         `dart <COMMAND_LINE_OPTION> --help`
