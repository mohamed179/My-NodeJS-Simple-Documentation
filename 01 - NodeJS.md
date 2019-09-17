# NodeJS

In this file we will talk about:
1. [What is NodeJS](#what-is-nodejs)
1. [NodeJS History](#nodejs-history)
1. [V8 JavaScript Engine](#v8-javascript-engine)
1. [NodeJS Bindings](#nodejs-bindings)


## What is NodeJS

[Node.js](https://nodejs.org) is an open-source, cross-platform, JavaScript run-time environment that executes JavaScript code outside of a browser.

Node.js is a c++ program that can run JavaScript outside browsers.

Node.js uses  [Chrome's V8 JavaScript engine](https://v8.dev/) to run JavaScript Nodejs send V8 the th JavaScript code then V8 convert this code to **_machine code_** which can run on machine used.

NodeJS uses an event-driven, **_non-blocking I/O model_** that makes it lightweight and efficient.


## NodeJS History

NodeJS was written initially by Ryan Dahl in 2009.


## V8 JavaScript Engine

V8 is Google’s open source high-performance JavaScript and WebAssembly engine, written in C++. It is used in Chrome and in Node.js, among others. It implements ECMAScript and WebAssembly, and runs on Windows 7 or later, macOS 10.12+, and Linux systems that use x64, IA-32, ARM, or MIPS processors. V8 can run standalone, or can be embedded into any C++ application.


## NodeJS Bindings

Not all NodeJS features are JavaScript features, NodeJS has many features that not JavaScript features such as file system.

Those features not implemented by V8, but NodeJs provides V8 with the c++ implementations of those features.

When executing an application, NodeJS pass V8 the JavaScript code, implementations of the NodJS self features and the context of how V8 can use those implementations.