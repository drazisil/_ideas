https://twitter.com/drazisil/status/955531971014381574

Looking for a #NodeJS logger that will know what line it ran on. 

Bonus points if it can detect if it's in a function and prefix the line.

-------

https://www.npmjs.com/package/logtrace looks perfect, but hasn't been touched in a while and no longer exists on GitHub. 
I've contacted the author to see if they would be ok with me taking it over.

If not, this SO answer looks promising https://stackoverflow.com/questions/14172455/get-name-and-line-of-calling-function-in-node-js

----------

LogTrace was made public and is still in use.

Both https://github.com/nherment/logtrace and https://github.com/Portchain/logacious do what I want, but both use the `arguments.callee` https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments/callee property, which is not legal in strict mode.

I'm going to try to make a valid one. Idealy as a plugin/wraper to https://github.com/winstonjs/winston
