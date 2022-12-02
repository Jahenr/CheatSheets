# Flutter

   CheatSheet

      # confirm if your flutter SDK is set up correctly and compatible with other platforms, devices and IDE.
         `flutter doctor` or `flutter doctor -v`


      # create a new flutter project from terminal
         `flutter create NAME_OF_APP`
      

      # create a new flutter project and replace the default package name flutter gives you com.example.myappname
         `flutter create –org com.mywebsite NAME_OF_APP`


      # set a specific language for the Android app and iOS; here we use Java for Android and objective-C for iOS
         `flutter create --org=com.mywebsite --android-language=java --ios-language=objc NAME_OF_APP`


      # mistakenly deleted a file, create it with its boilerplate codes. This will replace all missing files without creating everything from scratch
         `flutter create --no-overwrite --org=com.mywebsite.NAME_OF_APP`


      # list all devices connected and supported by the Flutter SDK
         `flutter devices`

      # get current device id
         `flutter --device-id`


      # flutter help
         `flutter -h`


      # run a flutter app
         `flutter run`


      # to see more outputs while app is trying to build in debug mode
         `flutter run -v `


      # after making stateless change(changing font size, color, widget size, shape, etc)
         `Hot Reload (r): tap small r while app is running`


      # after you make changes to class instances or things that will affect app’s current state
         `Hot Restart(R): tap big R while app is running`


      # take a screenshot from the terminal:
         `tap small (s) when running the app in debug mode`


      # lost connecting while debugging, connect your app back via
         `flutter attach -d <target-platform-name` or simply `flutter attach`


      # show all available options while your app is running in debug mode:
         `press small (h)`


      # list flutter channels.
         `flutter channel`


      # switch to a flutter channel
         `flutter channel CHANNEL_NAME`


      # upgrade your Flutter SDK with Dart
         `flutter upgrade`


      # get current flutter version
         `flutter --version`


      # list, launch or create emulators
         `flutter emulators`


      # generate localizations for the Flutter project
         `flutter gen-l10n PATH_TO_TRANSLATION_FILE`


      # format a dart file
         `flutter format PATH_TO_DART_FILE`


      # run your tests packages
         `flutter test PATH_TO_TEST_FILE`

      # add a third party package
         `flutter pub add NAME_OF_PACKAGE`


      #  download the third party package
         `flutter pub get`
      

      # remove every temporary files & folders
         `flutter clean`


      # build the APK file
         `flutter build apk`


      #Tip: speed up Flutter Development
         use the third packages to suit your needs. Google first.
