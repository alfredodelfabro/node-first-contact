# node-first-contact
This example API was created to study the very basic about Node.js. The tutorial was made by Traversy Media -- <cite>[Traversy Media - Node.js Crash Course (2024 Revamp)][3]</cite>.

# What I learned

In the next sessions I point it out what I've learned making the tutorial.

## Volta

As a Ruby and Ruby on Rails developer, I was used to install and manage Ruby versions with rvm or rbenv. I decided to use Volta in order to manage development environments for NodeJS projects.

> Similar to package managers, Volta keeps track of which project (if any) you’re working on based on your current directory. The tools in your Volta toolchain automatically detect when you’re in a project that’s using a particular version of the tools, and take care of routing to the right version of the tools for you.
> -- <cite>[Volta documentation][1]</cite>

[1]: https://docs.volta.sh/guide/understanding

## npm

NPM stands for Node Package Manager and it is used to manage libs and frameworks used by an application.

When a project is created using npm, a file named package.json is created that has all the packages used on the environment. Besides that, npm is a repository where other developers and companies distribute theis tools and libs that abstract a lot of code. It is something like gems in Ruby.

## Start a new application

We start a new application by typing `npm init`. This command creates a new `package.json` file to manage application.

## Using ES modules

To use ES modules we need to add `"type": "module"` on our package.json configuration. This allow us to use this syntax, for example, import from other files:

`import { getUser } from './userController';`

## Use nodemon on development

nodemon is a tool that helps develop Node.js based applications by automatically restarting the node application when file changes in the directory are detected -- <cite>[nodemon documentation][2]</cite>.

[2]: https://github.com/remy/nodemon

To use nodemon we need to run `npm install -D nodemon`. The `-D` flag is used to install only on development environment. See:

```
"devDependencies": {
  "nodemon": "^3.1.0"
}
```

We also need to change our package.json to indicates that we want to use nodemon to start the server:

```
"scripts": {
  "start": "nodemon server.js"
},
```

## How to start our application?

Just run `npm start`. Since we are using nodemon, we don´t need to reload the server every time we change a file.

## The use of .env file

This file is used to put some environment variables so you don't expose things like API keys and sensitive information on source code. This comes by default on recent versions of nodejs.

You just need to create the `.env` file and change the start script on package.json to use it:

```
"scripts": {
  "start": "nodemon --env-file=.env server.js"
},
```

## Tutorial by Traversy Media

<cite>[Traversy Media YT Channel][3]</cite>.

[3]: https://github.com/remy/nodemon