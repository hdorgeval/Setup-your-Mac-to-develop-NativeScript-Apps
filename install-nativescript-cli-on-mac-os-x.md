# Install NativeScript CLI on Mac OS X

The purpose of this section is to guide you to install the NativeScript CLI in your development environment. The NativeScript CLI provides a set of commands to create, build, and deploy NativeScript-based projects on iOS and Android devices.

The NativeScript CLI is a node package that you can install from node packet managernpm.

If you have no clue on how to install or where to find a node.js package, search for its name on [npm search](http://npmsearch.com/):

![](/assets/Screen Shot 2016-12-26 at 22.20.43.png)

In the found results list, select the NativeScript Command Line interface for building NativeScript projects :

![](/assets/Screen Shot 2016-12-26 at 22.22.21.png)

Click on thenativescriptlink. You will land on the [NativeScript Command-Line Interface GitHub page](https://github.com/NativeScript/nativescript-cli#readme).

Take time to read all detailed information supplied in this page.

Open the Terminal app and type:

```
npm install nativescript -g
```

Installation of the nativescript package is done globally. This will ensure you can use its command line tool in any Visual Studio Code project.

If you have trouble during package installation, have a look at [//docs.npmjs.com/getting-started/installing-npm-packages-globally](///docs.npmjs.com/getting-started/installing-npm-packages-globally).

If you receive the following error message:

```
Error: EACCES: permission denied, access '/usr/local/lib/node_modules'
```

have a look at : [https://docs.npmjs.com/getting-started/fixing-npm-permissions](https://docs.npmjs.com/getting-started/fixing-npm-permissions) to solve this issue.

Once installed, the name of this Command-Line tool is **tns**. Type the following command to have all details of this CLI:

```
tns -h
```

During the installation there is a check for the Android SDK installation. You may receive these messages in the Terminal window:

