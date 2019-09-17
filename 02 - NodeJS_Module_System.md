# NodeJS Module System

In this file we will talk about:
1. [What is NodeJS Module System?](#what-is-nodejs-module-system)
1. [Modules Types](#modules-types)
1. [NodeJS Core Modules](#nodejs-core-modules)
1. [NPM Modules](npm-modules)
1. [Our Own Modules](our-own-modules)


## What is NodeJS Module System?

In the Node.js module system, each file is treated as a separate module.

NodeJS import modules using `require()` function.

And export module by assigning the module object to `module.exports` object.


## Module Types

There are 3 types of module types:
* NodeJS core modules
* NPM modules
* Your own modules


## NodeJS Core Modules

NodeJS has several modules compiled into the binary.

The core modules are defined within NodeJS's source and are located in the `lib/ folder`.

Core modules are always preferentially loaded if their identifier is passed to `require()`. For instance, `require('fs')` will always return the built in File System `fs` module, even if there is a file by that name.

One of the famous NodeJS core modules is file system `fs` module.

```javascript
const fs = require('fs');

fs.writeFileSync('names.txt', 'Mohamed, Ahmed, Kamal');
```

> **Note:** Its best practice to name the imported object as module name


## NPM Modules

NPM (NodeJS Package Manager) is the default package manager for NodeJS. It has billions of packages that can be used in our application only by including (installing) them.

To use npm packages, we first need to initate npm in our application as follows:

```bash
$ npm init
```

this will initiate npm use in your application by adding `package.json` file if not exist.

Then to install a npm package run the following command:

```bash
$ npm install [package-name]@[version]
```

`npm install package-name` will install the package by creating a new directory `node_modules`if not exist and set the module folder in this folder and add this packge to the dependencies arry in `package.js` file.

To import a npm package, we use `require()` function as follows:

```javascript
const packageName = require('package name');
```

> **Note:** Its best practice to name the imported object as package (module) name

Also, we can install npm packages globally by using `-g` flag as follows:

```bash
$ npm install [package-name]@[version] -g
```

This will add the package to the NodeJS Modules and can be used in any application installed in your machine as any NodeJS core modules you have.


## Our Own Modules

We can import our modules using `require()` function as follows:

```javascript
const moduleName = require('module path');
```

And, we can add a variable to the current module by adding it as a property to the `module.exports` as follows:

```javascript
const var1 = 'value';
const var2 = 'another value';
module.exports.var1 = var1;
module.exports.var2 = var2;
```

or simply we can assign an object to `module.exports` as follows:

```javascript
const objectName = {
  // object content ...
};
module.exports = objectName;
```

> **Note:** we can access `module.exports` by simply type `exports`