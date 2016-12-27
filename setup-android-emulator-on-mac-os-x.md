# Setup Android Emulator on Mac OS X

The purpose of this section is to guide you to create in your development environment an Android emulator.

Android emulators are managed through a UI called AVD Manager

AVD Manager has a nice interface when started from Android Studio.

Start Android Studio app, then create a blank project.

Go to the Tools menu -&gt; :Android -&gt; AVD Manager:

![](/assets/Screen Shot 2016-12-27 at 16.47.56.png)

If no emulator has been created you should start with this screen:

![](/assets/Screen Shot 2016-12-27 at 16.51.24.png)

Click the Create Virtual Device button.

In the Select Hardware window , select Nexus 5 as shown in the following snapshot:

![](/assets/Screen Shot 2016-12-27 at 16.52.58.png)

Click the Next button.

In the System Image, select the system image Nougat, API Level 25 , ABI x86 :

![](/assets/Screen Shot 2016-12-27 at 16.57.28.png)

Click on the download link to download the selected System Image. This download process is done through SDK Manager.

Once the download is complete, click on the Next button.

In the Verify Configuration window, check any parameter :

![](/assets/Screen Shot 2016-12-27 at 18.07.01.png)

Then click on the Finish button.

AVD Manager shows you the newly created device:

![](/assets/Screen Shot 2016-12-27 at 18.17.00.png)

Click on the launch button to launch the newly created AVD in the emulator.  
Notice in the Run Window of Android Studio the command line used to start the device:

```
/Users/HDO/Library/Android/sdk/tools/emulator -netdelay none -netspeed full -avd Nexus_5_API_25
```

which can be shortened to :

```
$ANDROID_HOME/tools/emulator -netdelay none -netspeed full -avd Nexus_5_API_25
```

## How to start Android Emulator from Terminal?

Stop the emulator started by Android Studio. Open the Terminal app and type the following command:

```
$ANDROID_HOME/tools/emulator -netdelay none -netspeed full -avd Nexus_5_API_25
```

This should start the emulator with the selected AVD.

