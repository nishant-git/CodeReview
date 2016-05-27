Java/Android  Code Styles and lint
================

IntelliJ IDEA code style settings for Java and Android studio projects.

The [code styles](https://source.android.com/source/code-style.html) below are strict rules, not guidelines or recommendations. Contributions to Android that do not adhere to these rules are generally not accepted. We recognize that not all existing code follows these rules, but we expect all new code to be compliant.

Install jar and configure:
----------------------

    Import settings.jar into Android Studio. It defines our coding standard.
    you just need to use File -> Import Settings option in Android Studio.

Or Install using script
-------------------------

 * On Unix, run the `install.sh` script. Windows users should use `install.bat` instead.
 * Restart IntelliJ if it's running.
 * Open IntelliJ Project Settings -> Code Styles, change the code style for the
   project to the one you want.

How to use lint
----------
In Android Studio, the configured Lint and IDE inspections run automatically whenever you build your app.

With Android Studio, you can also run Lint inspections for a specific build variant, or for all build variants from the `build.gradle` file. Add the lintOptions property to the android settings in the build file. This code snippet from a Gradle build file shows how to set the quiet option to true and the abortOnError option to false.

```
android {
    lintOptions {
       // set to true to turn off analysis progress reporting by lint
       quiet true
       // if true, stop the gradle build if errors are found
       abortOnError false
       // if true, only report errors
       ignoreWarnings true
       }
       ...
    }
```

To manually run inspections in Android Studio, from the application or right-click menu, choose **`Analyze > Inspect Code`**. The Specify Inspections* Scope dialog appears so you can specify the desired inspection scope and profile.

License
-------

[![Public domain](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/legalcode)
