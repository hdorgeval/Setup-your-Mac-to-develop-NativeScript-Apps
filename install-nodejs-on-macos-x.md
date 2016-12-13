# Install Node.js v7.2.1 on Mac OS X

The purpose of this section is to guide you to install Node.js in your development environment. Node.js is both a runtime and a framework. As a runtime, Node.js manages the execution of JavaScript code on the machine where it is installed. This machine could be a server in the cloud or could be any machine like your development machine.

Node.js provides a framework that you can use to develop connected JavaScript application.

Node.js provides an extensibility mechanism called Module.

Node.js itself is designed as a set of core modules.

To install and use third-party modules you need a package installer. This package installer is called npm \(Node Packet Manager\). Though npm and Node.js are provided by two different legal entities, the node packet manager npm is bundled with the Node.js installer.

Latest current version for node.js \(7.2.1\) and npm \(3.10.10\) is available at: [https://nodejs.org/en/download/current/](https://nodejs.org/en/download/current/).

Select the Macinstosh Installer Icon:

![](/assets/Screen Shot 2016-12-12 at 23.14.17.png)

Open your Downloads folder and double clic on the node-v7.2.1.pkg file.

The Node.js installer starts on the Introduction screen:

![](/assets/Screen Shot 2016-12-12 at 23.18.47.png)

Click on the Continue button.

On the Licence screen click on the Continue button and agree the licence.

On the Destination Select screen, The Install for all users on this computer should be selected:

.![](/assets/Screen Shot 2016-12-12 at 23.23.59.png)

Clic on the Continue button.

On the Installation Type screen, select the standard installation type:

![](/assets/Screen Shot 2016-12-12 at 23.27.36.png)

Clic the Install button.

You may eed to enter your password.

At the end of the installation, you receive the Summary screen:

![](/assets/Screen Shot 2016-12-12 at 23.32.19.png)

To make sure that /usr/local/bin is in the $PATH environment variable, open a Terminal window and type the following command

`echo $PATH`

Finally clic the Close button.

## How to check if Node.js is correctly installed and what is the installed version?

Open a terminal Window and type the following command

`node -v`

It should output `v7.2.1 or any version number of the current Node.js installation.`

## How to check if npm is correctly installed and what is the installed version?

Open a terminal Window and type the following command

`npm -v`

It should output `3.10.10` or any version number of the current npm installation.

## What is Node.js CLI?

Node.js is a command-line application. This means it has no user interface. You typically invoke Node.js inside a Terminal window.

Command-line applications are often called CLI.

Node.js provides a CLI which is an executable file called `node`. This executable file is located in folder `/usr/local/bin`.

To invoke this command-line, open a Terminal window and type the following command:

`node -h`

This will give you the syntax to execute a JavaScript file

```
Usage: node [options] [ -e script | script.js ] [arguments]

node debug script.js [arguments]
```

## What is npm CLI?

npm is a command-line application. This means it has no user interface. You typically invoke npm inside a Terminal window.

npm provides a CLI which is an executable file called npm. This executable file is located in folder `/usr/local/bin` and is a symbolic link to `/usr/local/lib/node_modules/npm/bin/npm`

To invoke this command-line, open a Terminal window and type the following command:

npm`-h`

  


