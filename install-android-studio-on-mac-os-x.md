# Install Android Studio on Mac OS X

The purpose of this section is to guide you to install in your development environment all the dependencies for Android development.

The fastest way is to download and install Android Studio.

Latest current version for Android Studio is available at: [https://developer.android.com/studio/index.html](https://developer.android.com/studio/index.html)

Select the Installer Icon:

![](/assets/Screen Shot 2016-12-26 at 19.27.31.png)

To install Android Studio on your Mac, proceed as follows:

1. Launch the Android Studio DMG file.
2. Drag and drop Android Studio into the Applications folder, then launch Android Studio.
3. Select whether you want to import previous Android Studio settings, then click OK.
4. The Android Studio Setup Wizard guides you though the rest of the setup, which includes downloading Android SDK components that are required for development.

![](/assets/Screen Shot 2016-12-26 at 23.21.50.png)  
Click the Next button.

![](/assets/Screen Shot 2016-12-26 at 23.23.04.png)

Select a Standard installation and click Next.

On the Verify Settings window, click Finish.

Once installed, you get the Welcome to Android Studio window :

![](/assets/Screen Shot 2016-12-27 at 00.01.25.png)

Click on the Configure Button and select SDK Manager:

![](/assets/Screen Shot 2016-12-27 at 11.22.42.png)

In the left pane select Android SDK. On the right pane, select the SDK Platforms Tab and select the SDKs for API level 22 up to 24.

Click the OK button to download and install these Android SDKs.

After accepting the licence you should see the following screen:

![](/assets/Screen Shot 2016-12-27 at 11.05.06.png)

Wait until all components are installed.

## Setup the ANDROID\_HOME system variable

Open the SDK Manager and make a copy of the Android SDK Location :

![](/assets/Screen Shot 2016-12-27 at 11.32.50.png)

Open the Terminal app and type the following command:

```
export ANDROID_HOME=/Users/HDO/Library/Android/sdk
```

To check the ANDROID\_HOME is correctly setup type the following commands:

```
cd $ANDROID_HOME
ls
```

You should see the following result:

```
add-ons        extras        patcher        platforms    system-images
build-tools    licenses    platform-tools    sources        tools
```

## Persist the ANDROID\_HOME system variable for the current user

The ANDROID\_HOME system variable must be persisted when you leave and resstart a new Terminal  Window.

One way to do this is to create or update a .profile file in the user's home directory. This file should contain all the commands that should be executed before the Terminal Window session starts.

Open the Terminal app and type the following commands:

```
cd $HOME
nano .profile
```

In the Text Editor, add the following line

```
export ANDROID_HOME=/Users/HDO/Library/Android/sdk
```

You should have a screen similar to the following screenshot:

![](/assets/Screen Shot 2016-12-27 at 15.43.53.png)

To save the .profile file, type `CTRL + X`, then type `Y` followed by the `ENTER` key.

Once done, quit the Terminal window, reopen a new one and type the following command to check if the system variable has been persisted:

```
echo $ANDROID_HOME
```

You should have a non empty response.



## References

[https://support.apple.com/en-us/HT202292](https://support.apple.com/en-us/HT202292)

