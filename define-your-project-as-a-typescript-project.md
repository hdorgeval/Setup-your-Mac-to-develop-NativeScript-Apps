### Define your project as a TypeScript project {#define-your-project-as-a-typescript-project}

[Typescript](http://www.typescriptlang.org/) is a de-facto standard for developing JavaScript Apps with Node.js, NativeScript and Angular2.

Visual Studio Code is language agnostic. You must give Visual Studio specific information to properly manage your code files.

To tell Visual Studio Code that you want to code with the TypeScript language, you must do two things:

* Download the TypeScript package;
* run the tsc --init command.

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

bla

