# NodeJS Command Line Arguments

In this file we will talk about:
1. [What is NodeJS Command Line Arguments?](#what-is-nodejs-command-line-arguments)
1. [Benefits](#benefits)
1. [How to access Them?](how-to-access-them)


## What is NodeJS Command Line Arguments?

NodeJSCommand line arguments are strings of text used to pass additional information to a program when an application is run through the command line interface (CLI) of an operating system. Command line arguments typically include information used to set configuration or property values for an application.

In most cases the arguments are passed after the program name in your prompt. An example of the syntax of command line arguments looks like this:

```bash
$ node [options] [V8 options] [script.js | -e "script" | -] [--] [arguments]
```

The arguments are usually separated by a space - however there are some runtimes that use commas to distinguish between multiple command line arguments. Also, depending on the program, you can pass arguments in the form of key-value pairs, which we'll see later in this article.


## Benefits

The following are some of the major benefits of using command line arguments:

* You can pass information to an application before it starts. This is particularly useful if you want to perform large number configuration settings.
* Command line arguments are passed as strings inputs that can be parsed into other data types.
* You can pass unlimited number of arguments via the command line.
* Command line arguments are used in conjunction with scripts and batch files, which is particularly useful for automated testing.


## How to access Them?

We can access command line argument by using `process.argv` array as the follows example:

```javascript
console.log(process.argv[2]);
// this will output the first argument
```

The `process.argv` array provide two strings as the first two elements and they are:

1. the path from where the node run `process.argv[0]`
1. the path of the executing script `process.argv[1]`

, and the rest of the elements are the command line arguments provided