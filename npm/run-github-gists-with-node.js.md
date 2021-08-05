# Run GitHub gists with Node.js

Gist-based Node.js scripts can be downloaded and invoked directly with `npx`. Check out this [example](https://gist.github.com/acostalima/95714b3263ecbd52109db3d1b494fd13), a script which copies to the clipboard a list with of all the extensions installed in Visual Studio Code. You can run the script with the follow command:

```bash
$ npx https://gist.github.com/acostalima/95714b3263ecbd52109db3d1b494fd13
```

Simple, right? This is useful to quickly share some code with someone else instead of setting up an entire repository. 

In order to successfully run any script, the following is required:

* Add the shebang `#!/usr/bin/env node` at the top of the script to explicitly tell the shell to use Node.js to run it.
* Create a `package.json` file to declare the dependencies the script uses.
* Add a [`bin`](https://docs.npmjs.com/cli/v6/configuring-npm/package-json#bin) property in the `package.json` to tell `npm` the script is an executable file.

> About npx: [https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b)



