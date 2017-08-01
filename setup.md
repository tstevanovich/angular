# Angular Setup

## Terminal
For Mac users, you should already have terminal installed. Windows users, I'd recommend [Cmder](http://cmder.net). This is preferable than using Windows command prompt.

## Editor
[Atom](https://atom.io) is the IDE we'll use.

## Atom packages
Atom comes with a whole bunch of packages to make editing code easier, and it also comes with a few annoying ones. Below is a list of packages I'd recommend on adding to it, and a couple to disable. Go to Atom settings `CTRL + ,`

<strong>Disable</strong>
<ul>
  <li>Welcome - Don't want to see the startup page each time you start the editor</li>
  <li>Wrap Guide - This put a horrible vertical line across the page</li>
</ul>

<strong>Install</strong>
<ul>
  <li>atom-typescript</li>
  <li>busy-signal</li>
  <li>editorconfig</li>
  <li>file-icons</li>
  <li>intentions</li>
  <li>linter</li>
  <li>linter-jshint</li>
  <li>linter-ui-default</li>
  <li>markdown-preview-plus</li>
  <li>color-picker</li>
  <li>emmet</li>
  <li>atom-bootstrap3</li>
</ul>

## Install Node
Let's check to see if you have Node installed. Go to the command line type `node -v`

You should see something like `v6.11.1`

If you don't have node then let's [install it](https://nodejs.org/en/download)

## NPM
NPM is the default package manager for the JavaScript runtime environment Node.js. NPM automatically comes with the node.js install

See what version you are on `npm -v`

## Change NPM Permissions
You'll more than likely get EACCES errors when using global packages. The best way to fix this is modifying the permissions on npm's directory

Let's find out the directory where npm is installed `npm config get prefix`

Find out what user you are logged in as `whoami`

Change directory to where npm is installed and change the ownership to you if it's not already done. `sudo chown -R $(whoami) $(npm config get prefix)`

## Modify Your NPM Config File
Go to your home directory, more than likely `cd /Users/<yourusername>`

There should be a .npmrc file here. If not type `touch .npmrc`

Here you can put your proxy settings and other user specific information if needed. Here is a list of [configs](https://docs.npmjs.com/misc/config).

## Install Angular
`npm install -g @angular\cli`

## Create a new project
`ng new nameofproject`

## View your project through a browser
`cd nameofproject`

`npm start`

The app will be viewable at [http://localhost:4200](http://localhost:4200)
