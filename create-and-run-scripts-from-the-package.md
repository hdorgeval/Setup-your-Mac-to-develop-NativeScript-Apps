### Create and run scripts from the package {#create-and-run-scripts-from-the-package}

In the previous section you started to dig into the scripts entry of the package.json file.

This entry represents a JavaScript literal object with one default property called test. This object is a way to extend the commands set of npm.

Go back to the opened Terminal window and type the following command:

```
npm test
```

You can use the scripts object to start any app. To do this add the following property to the scripts object:

```
"myCommand" : "siri"
```

Thepackage.jsonfile should look like :

