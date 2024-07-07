# 1. Running Native C/C++ code in Node.js

I created this simple API to allow code written in C/C++ to run in Node.js.
This type of API will come in handy when the need to compile complex operations such as those of Linear Algebra or CompVision arises.

I am going to work on setting this project up for TypeScript & create a container for it to avoid software incompatibilities across platforms.

More updates to follow

## 2. Installation of app

Make sure you have the latest long-term support version of Node (v 18.+) & a supported version of Python.

Install the gcc/g++ compiler for Node.js, node-gyp globally

`npm install -g node-gyp`

If you are using Windows, make sure you execute this command before installing node-gyp globally:

`npm install --global --production windows-build-tools`

Compile C/C++ code by executing `npm run build`
Ideally, the instruction above replaces `node-gyp configure` && `node-gyp build`

To compile new code in the addon file, clear the build, re-configure, and re-build with `node-gyp clear`