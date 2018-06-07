# Angular Setup

## Terminal

For Mac users, you should already have terminal installed. Windows users, I'd recommend [GITbash](http://git-scm.com). This is preferable than using Windows command prompt.

## Editor

[Visual Studio Code](https://code.visualstudio.com/Download)

## Visual Studio Code Extensions

VSC comes with many extensions to make editing code easier. Below is a list of extensions I'd recommend on adding to it. Click on the extensions tab in your editor to begin searching and installing.

<strong>Install</strong>

<ul>
  <li>Angular Material 2, Flex layout 1, Covalent 1 &amp; Material icon snippets</li>
  <li>Angular v6 Snippets</li>
  <li>Auto Import</li>
  <li>Bracket Pair Colorizer</li>
  <li>Debugger for Chrome</li>
  <li>Markdown All in One</li>
  <li>Prettier - Code formatter</li>
  <li>TSLint</li>
  <li>Visual Studio Code Commitizen Support</li>
</ul>

## Editor settings (.editorconfig)

```
root = true

[*]
charset = utf-8
indent_style = space
indent_size = 2
insert_final_newline = true
trim_trailing_whitespace = true

[*.md]
max_line_length = off
trim_trailing_whitespace = false
```

## Prettier settings (.prettierrc)

```json
{
  "arrowParens": "avoid",
  "bracketSpacing": true,
  "disableLanguages": ["vue"],
  "eslintIntegration": false,
  "ignorePath": ".prettierignore",
  "jsxBracketSameLine": false,
  "printWidth": 80,
  "proseWrap": "preserve",
  "requireConfig": false,
  "semi": true,
  "singleQuote": true,
  "stylelintIntegration": false,
  "tabWidth": 2,
  "trailingComma": "none",
  "useTabs": false
}
```

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
