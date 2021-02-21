[Home](../README.md)

# Heroku Notes

## Defining and Application

Heroku lets you deploy, run and manage applications written in `Ruby`, `Node.js`, `Java`, `Python`, `Clojure`, `Scala`, `Go` and `PHP`.

An application is a collection of source code written in one of these languages, perhaps a framework, and some dependency description that instructs a build system as to which additional dependencies are needed in order to build and run the application.

## Knowing what to execute

You don’t need to make many changes to an application in order to run it on Heroku. One requirement is informing the platform as to which parts of your application are runnable.

If you’re using some established framework, Heroku can figure it out. For example, in Ruby on Rails, it’s typically rails server, in Django it’s `python <app>/manage.py` runserver and in Node.js it’s the main field in package.json.

Heroku is a polyglot platform – it lets you build, run and scale applications in a similar manner across all the languages – utilizing the dependencies and Procfile. The Procfile exposes an architectural aspect of your application and this architecture lets you, for example, scale each part independently. An excellent guide to architecture principles that work well for applications running on Heroku can be found in Architecting Applications for Heroku. 

## Deploying applications

Git is a powerful, distributed version control system that many developers use to manage and version source code. The Heroku platform uses Git as the primary means for deploying applications (there are other ways to transport your source code to Heroku, including via an API).

When you create an application on Heroku, it associates a new Git remote, typically named heroku, with the local `Git` repository for your application.

As a result, deploying code is just the familiar `git push`, but to the heroku remote instead:

[Deploy via Git](img/heroku-deploy.png)

## Building applications

When the Heroku platform receives the application source, it initiates a build of the source application. The build mechanism is typically language specific, but follows the same pattern, typically retrieving the specified dependencies, and creating any necessary assets (whether as simple as processing style sheets or as complex as compiling code).

## Running applications on dynos

Heroku executes applications by running a command you specified in the Procfile, on a dyno that’s been preloaded with your prepared slug (in fact, with your release, which extends your slug and a few items not yet defined: config vars and add-ons).

## Config vars

An application’s configuration is everything that is likely to vary between environments (staging, production, developer environments, etc.). This includes backing services such as databases, credentials, or environment variables that provide some specific information to your application.

Heroku lets you run your application with a customizable configuration - the configuration sits outside of your application code and can be changed independently of it.

## Source
[How Heroku Works](https://devcenter.heroku.com/articles/how-heroku-works)