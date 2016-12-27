### Create and run scripts from the package {#create-and-run-scripts-from-the-package}

In the previous section you started to dig into the scripts entry of the package.json file.

Have a look to the scripts entry \(line 6 and 7 of the above screen shot\). This entry represents a JavaScript literal object with one default property called test. This object is a way to extend the commands set ofnpm.

Go back to the opened Command Prompt and type the following command:

```
npm test
```

You can use the scripts object to start any executable. To do this add the following property to the scripts object:

```
"myCommand" : "notepad"

```

Thepackage.jsonfile should look like :

