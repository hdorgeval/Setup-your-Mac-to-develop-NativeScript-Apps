# Visual Studio Code installation {#visual-studio-code-installation}

The purpose of this section is to guide you to install Visual Studio Code in your development environment. Visual Studio Code is good choice to develop, debug and deploy JavaScript, TypeScript and NativeScript Apps.

Visual Studio Code is a brand new cross-platform IDE from Microsoft.

Visual Studio Code does not rely on predefined project templates to create a project. You can create your own project templates. You can create your own build process. You can debug. You have IntelliSense on JavaScript , it's Typescript oriented by default.

Install from [https://code.visualstudio.com](https://code.visualstudio.com/)

Click on the Download for Mac button:

![](/assets/Screen Shot 2016-12-13 at 22.43.47.png)

Then follow installation steps from : [Running VS Code on Mac](https://code.visualstudio.com/docs/setup/mac)

## How to start Visual Studio Code from Terminal window?

Visual Studio Code projects are folder based. This means that Visual Studio Code must run in the context of your project folder.

One way to achieve this is to open a Terminal window, then cd to your project folder  and then type `code .` to start Visual Studio Code in the context of the current directory.

For this to work a symbolic link file named `code` must be created in the /usr/local/bin  folder:

* Start Visual Studio Code from the Applications folder;

* Open the Command Palette\(⇧⌘P\) and type`shell command`to find the Shell Command: Install 'code' command in PATH command.

![](https://code.visualstudio.com/images/mac_shell-command.png "Mac shell commands")

After executing the command, restart the terminal for the new`$PATH`value to take effect. You'll be able to simply type 'code .' in any folder to start editing files in that folder.

