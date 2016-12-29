### Configure TypeScript to work with external modules {#configure-typescript-to-work-with-external-modules}

For sure, you will develop your application by using one or more third-party node.js packages. You will install these packages in your project by invoking the [npm install](https://docs.npmjs.com/cli/install) command.

These packages are stored as sub-folders within the node\_modules folder. The node\_modules folder lives at the root of your project's folder.

But there are modules that you cannot download with the npm package manager. These modules are all the core modules provided by node.js itself. These node.js core modules are described in the node.js [API documentation](https://nodejs.org/dist/latest-v6.x/docs/api/).

Among these modules you have:

* http
  * The http module enables to use the HTTP server and client
* net
  * The net module enables to implement web socket for asynchronous dual-channel communication between client and server
* path
  * The path module provides utilities for working with file and directory paths

These core modules are provided by node.js at runtime. Therefore, these modules are unknown modules at design-time  for Visual Studio Code.

To work with these core modules by using the JavaScript syntax, you will write:

```
const http = require('http');
const net = require('net');
const url = require('path');
```

In TypeScript the require\(\) syntax is replaced by an import syntax:

```
import * as http from "http";
import * as net from "net";
import * as path from "path";
```

In Visual Studio Code, create a folder called **app** in your project's folder. Then create an **app.ts** file within the app folder. In the app.ts write the following statement:

```
import * as http from "http";
```

You will notice that Visual Studio complains it cannot find the http module:

![](/assets/Screen Shot 2016-12-29 at 11.38.53.png)

To work with the core Node.js modules, Visual Studio needs a type definition for these modules. A type definition is a file with the **.d.ts** extension. A type definition provides information about the method and properties that you can use. In one word it describes the public interface of the module.

To install these files in your project you will use a node package called [typings](https://github.com/typings/typings).

To install this package, open a Terminal Window from Visual Studio Code and type the following commands:

```
npm install typings --save-dev

npm install typings --global
```

The **--save-dev** option means this package is a development dependency for your project. It also means the typings package does not need to be deployed to the production or to the target environment.

The typings package is also deployed globally because it exposes a CLI. You will use this CLI to download and install, in your project folder, any needed type definition file.

You will use this CLI to configure your project folder. To do this type the following command in the same Terminal window:

```
typings init
```

This command create a **typings.json** file in the project's folder.

Now you are ready to download and install the type definition file for node.js core modules. To do this type the following command in the Terminal window opened by visual Studio Code:

```
typings install dt~node --global --save-dev
```

To discover the different options and the syntax of the install command provided by the typings CLI, you can type:

```
typings install -h
```

This command first creates a **typings** folder within the project's folder. It then downloads the **node.d.ts** file inside that folder. It also creates or updates an **index.d.ts** that references all downloaded type definition files. It registers in the **typings.json** the **node.d.ts** file as a development dependency. You can download or re-download all type definition files declared in the typings.json file by invoking the command:

```
typings install
```

Open the **app.ts** file. You will see that Visual Studio does not complain anymore. If you start typing http., the IntelliSense helps you to complete your code:

![](/assets/Screen Shot 2016-12-29 at 11.57.04.png)

bla



