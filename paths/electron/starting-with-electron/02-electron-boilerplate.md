---
layout: simple-class
help: https://github.com/githubschool/on-demand-electron-app/issues/new?title=I%20need%20help&body=Describe%20what%20you%20need%20help%20with%20here.&labels=Help%20Wanted
header:
  overlay_image: cover.jpeg
  overlay_filter: rgba(46, 129, 200, 0.6)
title: Create your app
permalink: /electron/create-an-app/create-your-app/
next-page: /electron/create-an-app/push-your-project-to-github/
facilitator: false
sidebar:
  nav: "create-an-app-in-electron"
main-content: |

  To begin, we will set up a base electron app using an npm package called [electron-forge](https://electronforge.io/).

  _Note: Electron Forge isn't the only way to get started with Electron! There are other resources, like [Electron Quick Start](https://github.com/electron/electron-quick-start)._

  To get started, we need to go through a few steps.

  ![gif of following the directions below](<% SITEURL %><% BASEURL %>/images/gifs/electron/electron1-createapp.gif)

  1. Find the terminal and navigate to your desired project location, for example: `cd ~/` will navigate to your home directory.
  1. Install electron-forge globally: `npm install -g electron-forge`
  1. Initialize a new project: `electron-forge init electron-app`
  1. Change into that app's directory: `cd electron-app`

  Important files to watch out for in any Electron app:

  - `package.json`
  - `package-lock.json`
  - `src/index.html`
  - `src/index.js`

show-me-how:
tell-me-why: |
  Any Electron app has [2 types of processes](https://github.com/electron/electron/blob/master/docs/tutorial/quick-start.md) that interact with each other. The main process, initialized by `package.json`, and a renderer process generated by each web page.

  - `package.json` - Points to the app's main file and lists your project's details and dependencies.
  - `package-lock.json` - If you're using NPM 5 or greater (you can check by running `npm -v`), you'll also get a [`package-lock.json` file](https://docs.npmjs.com/files/package-lock.json). This file aims to keep versions of dependencies identical across projects.
  - `src/index.html` - A web page to render. Each web page will spin off its own renderer process.
  - `src/index.js` - The default script called by `package.json` to create windows and handle system events. Runs the app's main process.

  #### What is Node?
  Node.js is the server side portion of full stack Javascript. Many websites are powered with Node, and it powers things on Electron as well. [Node.js documentation](https://nodejs.org/en/docs/) is full of information that explain its functionality and purpose.

  #### What is `npm`?
  `npm`, short for "Node Package Manager", is exactly as it is named: a manager for packages in Node. Dependencies and their versions are managed in apps through the `package.json` file, and downloaded through `npm`.
---
