# node-first-contact
Study the very basic about NodeJS to create an API.


# What I learned

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

