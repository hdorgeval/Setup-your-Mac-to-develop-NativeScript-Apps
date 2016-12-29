### Define your project as a TypeScript project {#define-your-project-as-a-typescript-project}

[Typescript](http://www.typescriptlang.org/) is a de-facto standard for developing JavaScript Apps with Node.js, NativeScript and Angular2.

Visual Studio Code is language agnostic. You must give Visual Studio specific information to properly manage your code files.

To tell Visual Studio Code that you want to code with the TypeScript language, you must do two things:

* Download the TypeScript package;
* run the **tsc --init** command.

To install TypeScript type the following command:

```
npm install typescript --save-dev
```

You should type this command in the Terminal Window opened from Visual Studio Code.

This command uses the install command of npm. More details about this command are provided at [https://docs.npmjs.com/cli/install](https://docs.npmjs.com/cli/install).

The --save-dev option means that TypeScript is a development dependency for your project. It makes sense since you will develop all your App in TypeScript.

A development dependency means you need this package to develop and debug your application. But you do not need this package in the target execution environment.

The npm install command did two things:

* It downloaded the package and all its dependencies within a sub folder of your project. This sub folder is called node\_modules. The node\_modules folder is the host for every npm packages you will install within your project;
* It updated the package.json file.

Go back to Visual Studio Code to see these two changes:

![](/assets/Screen Shot 2016-12-29 at 09.59.51.png)

A new folder called node\_modules is now present inside your project folder.

A new entry called devDependencies has been created in the package.json file.

Now you need to run the **tsc --init** command to tell Visual Studio Code you are coding in TypeScript.

Before typing this command, you need to know where this command is living.

The node\_modules folder has a **.bin** sub-folder and a typescript sub-folder. The typescript sub-folder contains the downloaded typescript package. The **.bin** folder contains commands or executable files related to the downloaded packages.

If you open the **.bin** folder you will see a **tsc** command. This **tsc** command is the TypeScript CLI. This means that any action related to TypeScript, like compiling to JavaScript, will be done through this command line.

Any command or executable file in the **.bin** folder can be invoked in two ways.

The first way is to open the .bin directory in a Terminal window and then call the CLI from this command window. To do this go back to Visual Studio and right-click the .bin folder then select the option Open in Terminal. In this Terminal window type **./tsc**: you will get the help for the TypeScript CLI.

But if you just type **tsc** in the Terminal window, you will get the following message:

```
tsc
tsc: command not found
```

To invoke the TypeScript CLI directly in the project Terminal window, the Typescript package must be installed globally.

To do this, type the following command:

```
npm install typescript --global
```

Now you can run the following command the Terminal window \(This Terminal window must be opened from the Command Palette of Visual Studio Code\) :

```
tsc --init
```

The **tsc --init** command creates a new file at the root of your project folder. The name of this file is **tsconfig.json**.

The **tsconfig.json** file tells Visual Studio that your project is a TypeScript project.

Go back to Visual Studio Code to see this new file:

![](/assets/Screen Shot 2016-12-29 at 11.05.33.png)

Learn more about **tsconfig.json** in next section.



