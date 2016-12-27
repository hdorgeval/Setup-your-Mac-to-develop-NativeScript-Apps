### Create and run scripts from the package {#create-and-run-scripts-from-the-package}

In the previous section you started to dig into the scripts entry of the package.json file.

This entry represents a JavaScript literal object with one default property called test. This object is a way to extend the commands set of npm.

Go back to the opened Terminal window and type the following command:

```
npm test
```

You can use the scripts object to start an Android emulator. To do this add the following property to the scripts object \(Go to section **Setup Android Emulator** for the details on how to setup this Android emulator\):

```
"Nexus5" : "$ANDROID_HOME/tools/emulator -netdelay none -netspeed full -avd Nexus_5_API_25"
```

The package.json file should look like :

![](/assets/Screen Shot 2016-12-28 at 00.10.24.png)

Save the package.json file.

To run your custom android emulator type the following command in the Terminal window:

```
npm run Nexus5
```

The scripts content is fully described at [https://docs.npmjs.com/misc/scripts](https://docs.npmjs.com/misc/scripts).

