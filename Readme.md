# Introduction to Web Apps with Vue

We're starting from basically nothing but HTML and working our way up to a full working web application.

We'll be using [Vue](www.vuejs.org) as your first introduction to web programming. We can use as little of it, or as much of it as we'd like, unlike other frameworks that demand complete control.

## Goals

These lessons use an intermediate level of HTML and CSS, but no understanding of either is required. This is about playing with code, doing something useful (or not) and having fun.

## Development Tools

You'll need the following tools to start development.

- Install and manage source code using [git](www.git-scm.org)
- Create a free account at [GitHub](www.github.com). You can create and manage your own projects on GitHub and allow others to view your code and help you debug.
- You'll need [the node ecosystem](www.nodejs.org) to download tools, frameworks and code libraries. [Download and install node](https://nodejs.org/en/download/) on your computer.
- I recommend Microsoft's [Visual Studio Code](https://code.visualstudio.com/download) as your editor. Download and install it on your computer. Once you start to edit code, it will recommend extensions and plug-ins to make your life much easier.
- Learn how to use your terminal program for the command line.

## How to start development

1. Start your terminal program. Navigate to a directory where you want to start development. I usually create a directory called `projects`, then create all my projects under that.
2. Type `git clone https://github.com/brianyamasaki/AppsWithVue`. This will download the source code to your machine in a directory named `AppsWithVue`.
3. Change your current directory into AppsWithVue by typing `cd AppsWithVue`.
4. Download your libraries and frameworks by typing `npm install`. This could take a few minutes to download everything.
5. Type `npm start` at a command prompt and the project will get compiled and a webserver will start serving the project. The server will continue to run until you stop it, either with a <ctrl>-c or if you terminate the command terminal.
6. Start a browser and browse to `localhost:4000`. You should see your website in the browser.

## What's in the project

The index.html at the base directory has no JavaScript, it's just a simple file with links to each of the versions.

### V0

We're starting with a simple HTML file with almost no styling, but a very basic application inside.

#### The Code

Inside the HTML, {{message}} is to be replaced by the contents of that named variable in the &lt;script&gt; statement.

### V1

We're adding a CSS framework called Bootstrap to help layout our web page. We're putting in a menu bar at top just because most projects that you create will need it.

## How the build system works

In case you were wondering, the npm environment gets recognized by the node environment you downloaded to your machine. When you cloned the source onto your filesystem and typed `npm install`, all kinds of tools and code got downloaded into a folder called node_modules.

1. When you type `npm start`, npm looks into a file called `package.json` and looks for a section called `scripts`. In that section, npm finds a line labeled `start` and executes the right side of the line into a command line. You can easily just type that line into your terminal to execute if you'd like.
2. Parcel starts a tool called Parcel-builder. Documentation on that tool can be found [here](https://parceljs.org/). Parcel-builder starts a web server that can be found at `localhost`. In this example, I've chose to put it at port 4000, thus `localhost:4000`. Parcel-builder actually cross compiles your code before it serves it, to guarantee that even simpler, older browsers can actually run your code. The compiled code is actually placed in the `dist` directory. In fact, it copies your entire project into `dist` and really only serves that directory.
