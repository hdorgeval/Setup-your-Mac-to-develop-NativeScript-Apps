# Your First NativeScript project with TypeScript

The purpose of this section is to give you the basic knowledge of how to create your own Visual Studio Code project with NativeScript and TypeScript. You will configure this project template to develop applications in TypeScript. You will learn how to use and execute the NativeScript CLI for a new project. You will learn how to setup Android and iPhone emulators to debug your application on those devices.

Going through this section will ensure your development environment is correctly setup for creating awsome NativeScript Apps.

### Create the root folder of your NativeScript project {#create-the-root-folder-of-your-project-template}

Within your home folder, create a folder called VSCodeProjects \(if not already done\). This folder will be the root folder for all your NativeScript applications developed with Visual Studio Code.

Open the Terminal app and type the following commands:

```
cd $HOME
cd VSCodeProjects
```

Then type the following command to create a new project folder by using the default TypeScript project template:

```
tns create MyApp --template typescript
```

This command will create a new folder called MyApp within the VSCodeProjects projects folder.

This MyApp folder will contain all the files needed to create a new NativeScript App.

## Build Your NativeScript Project for Android

Once the project is created, type the following commands in the Terminal window:

```
cd MyApp
tns platform add android
tns prepare android
tns build android
```

## Build Your NativeScript Project for iOS

Once the project is created, type the following commands in the Terminal window:

```
cd MyApp (only if you did not build for Android)
tns platform add ios
tns prepare ios
tns build ios
```

## Create Scrips to start Android and iPhone emulator

Open Visual Studio Code from the Terminal window:

```
code .
```

Within Visual Studio Code, open the package.json file and insert the following scripts section:

```
"scripts": {
    "Nexus5": "$ANDROID_HOME/tools/emulator -netdelay none -netspeed full -avd Nexus_5_API_25",
    "iPhone6" : "/Applications/Xcode.app/Contents/Developer/Applications/Simulator.app/Contents/MacOS/Simulator -CurrentDeviceID 8528838E-4B47-4F0E-B415-E87F8C8A6163"
  }
```

See the [Create and run scripts from the package](/create-and-run-scripts-from-the-package.md) for more details on how to create scripts to start Android and iOS emulators.

The package.json file should look like this:

![](/assets/Screen Shot 2016-12-29 at 19.23.11.png)

bla



