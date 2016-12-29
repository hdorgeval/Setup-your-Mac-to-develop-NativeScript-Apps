# Check NativeScript Installation is complete {#check-nativescript-installation-is-complete}

Checking if you environment is setup to develop NativeScript apps is very easy. 

Open a Terminal Window and type:

```
tns doctor
```

If the installation is OK you will receive this response:

```
NOTE: You can develop for iOS only on Mac OS X systems.
To be able to work with iOS devices and projects, you need Mac OS X Mavericks or later.

Your components are up-to-date.

No issues were detected.

```

If some components are missing from the android SDK you may receive this response:

```
Cannot find a compatible Android SDK for compilation. To be able to build for Android, install Android SDK 22 or later.
Run $ android to manage your Android SDK versions.

```

```
You need to have the Android SDK Build-tools installed on your system. You have to install version 23.
Run android from your command-line to install required Android Build Tools.

```

```
You need to have Android SDK 22 or later and the latest Android Support Repository installed on your system.
Run $ android  to manage the Android Support Repository.

```

If you see one of these messages, go to the[Android SDK installation](https://hdorgeval.gitbooks.io/nativescript/content/WindowsInstallation/WindowsInstallation/AndroidSdkInstallation.md)section to solve this issue.

