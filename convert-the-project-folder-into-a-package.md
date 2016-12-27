### Convert the project folder into a package

By default Visual Studio Code will see any files in the folder as unrelated files.  
To process your folder and any file within that folder as a project entity, Visual Studio Code needs specific information.

To do this, you need to transform your project folder into a package folder. From there you will be able to manage every dependencies in your project.  
You will be able to download and reference into your project folder any third-party module you need to develop your App.

Go to the Terminal Window you have opened in the previous section and type the following commands:

```
pwd
npm init --yes
```

the pwd command will give you your current working directory. Be sure this current directory is your project's directory.

Have a look to the npm CLI init command : [https://docs.npmjs.com/cli/init](https://docs.npmjs.com/cli/init)

What you get from this **init** command is new file called **package.json** created at the root of your project folder.

Go back to Visual Studio Code, the new **package.json** file has been dynamically loaded in the IDE.

Click on the **package.json** file, Visual Studio will open it in a separate window. It's content should look like :

![](/assets/Screen Shot 2016-12-27 at 22.13.41.png)

**Package.json** content is fully described at [https://docs.npmjs.com/files/package.json](https://docs.npmjs.com/files/package.json)

There are two entries within the **Package.json** that you must be aware of:

* The scripts entry;
* The main entry.

The main entry is the entry point of your package. The scripts entry is is a dictionary containing script commands that are run at various times in the lifecycle of your package.


