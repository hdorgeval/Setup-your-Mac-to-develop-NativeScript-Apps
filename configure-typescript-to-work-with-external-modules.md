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

