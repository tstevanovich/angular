# Angular Setup

## Programs to Download

- [Git w/ Gitbash](https://git-scm.com/downloads)
- [Visual Studio Code](https://code.visualstudio.com/Download)
- [Node with NPM](https://nodejs.org/en)
- [Augury](https://augury.rangle.io/)

## Terminal

For Mac users, you should already have terminal installed. Windows users, I'd recommend [GITbash](http://git-scm.com). This is preferable than using Windows command prompt.

## Editor

[Visual Studio Code](https://code.visualstudio.com/Download)

## Visual Studio Code Extensions

VSC comes with many extensions to make editing code easier. Below is a list of extensions I'd recommend on adding to it. Click on the extensions tab in your editor to begin searching and installing.

**Install**

- [Angular Essentials](https://marketplace.visualstudio.com/items?itemName=johnpapa.angular-essentials) - This automatically adds following extensions:
  - [Angular Console](https://marketplace.visualstudio.com/items?itemName=nrwl.angular-console)
  - [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template)
  - [Angular Snippets](https://marketplace.visualstudio.com/items?itemName=johnpapa.Angular2)
  - [angular2-inline](https://marketplace.visualstudio.com/items?itemName=natewallace.angular2-inline)
  - [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)
  - [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
  - [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
  - [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script)
  - [Peacock](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock)
  - [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
  - [TSLint](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-tslint-plugin)
  - [Winter is Coming Theme](https://marketplace.visualstudio.com/items?itemName=johnpapa.winteriscoming)
- [Auto Import](https://marketplace.visualstudio.com/items?itemName=steoates.autoimport)
- [Bracket Pair Colorizer](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer)
- [Git History](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)
- [Sass](https://marketplace.visualstudio.com/items?itemName=robinbentley.sass-indented)
- [SCSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-scss)
- [SVN](https://marketplace.visualstudio.com/items?itemName=johnstoncode.svn-scm)

## VS Code Settings (settings.json)

You can find this file in VS Code, by going to `File>Preferences>Settings`. In the upper right corder you'll see an icon that looks like `{ }` for Open Settings and it'll open your settings.json file. My settings.json looks like:

```json
{
  "git.autofetch": true,
  // Editor Settings
  "editor.codeActionsOnSave": {
    "source.organizeImports": true,
    "source.fixAll.tslint": true
  },
  "editor.tabSize": 2,
  // Prettier Settings
  "prettier.arrowParens": "always",
  "prettier.singleQuote": true,
  "prettier.printWidth": 100,
  // Peacock Settings
  "peacock.affectActivityBar": true,
  "peacock.affectStatusBar": true,
  "peacock.affectTitleBar": false,
  "peacock.keepBadgeColor": false,
  "peacock.keepForegroundColor": false,
  "peacock.favoriteColors": [
    {
      "name": "Angular Red",
      "value": "#b52e31"
    },
    {
      "name": "Auth0 Orange",
      "value": "#eb5424"
    },
    {
      "name": "Azure Blue",
      "value": "#007fff"
    },
    {
      "name": "Gatsby Purple",
      "value": "#639"
    },
    {
      "name": "JavaScript Yellow",
      "value": "#f9e64f"
    },
    {
      "name": "Mandalorian Blue",
      "value": "#1857a4"
    },
    {
      "name": "Node Green",
      "value": "#215732"
    },
    {
      "name": "React Blue",
      "value": "#00b3e6"
    },
    {
      "name": "Something Different",
      "value": "#832561"
    },
    {
      "name": "Vue Green",
      "value": "#42b883"
    }
  ],
  "[typescript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[html]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[scss]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
  "typescript.updateImportsOnFileMove.enabled": "always",
  "breadcrumbs.enabled": true,
  "svn.enableProposedApi": "product",
  "typescript.tsdk": "node_modules/typescript/lib",
  "workbench.iconTheme": "material-icon-theme",
  "workbench.colorTheme": "Winter is Coming (Dark Blue - No Italics)"
}

```

## Install Node

Let's check to see if you have Node installed. Open up command prompt and type `node -v`

You should see something like `v12.1.0`

If you don't have node then let's [install it](https://nodejs.org/en/download)

## NPM

NPM is the default package manager for the JavaScript runtime environment Node.js. NPM automatically comes with the node.js install

See what version you are on `npm -v`

## Install Angular

```bash
npm install -g @angular\cli
```

## Create a new project

This will install a new Angular project with SCSS for styling instead of the default CSS. It will also add Angular routing to the project.

```bash
ng new nameofproject --style=scss --routing
```

## Add prettier setting files

Navigate into your new project directory

```bash
cd nameofproject
touch .prettierrc
touch .prettierignore
```

### Prettier settings (.prettierrc)

```json
{
  "useTabs": false,
  "printWidth": 80,
  "tabWidth": 2,
  "singleQuote": true,
  "trailingComma": "none",
  "semi": true,
  "arrowParens": "always"
}
```

### Prettier ignore file (.prettierignore)

```json
package.json
package-lock.json
dist/
```

## Add extra dev dependencies to package.json

```bash
npm install --save-dev prettier
npm install --save-dev pretty-quick
npm install --save-dev tslint-angular
npm install --save-dev tslint-config-prettier
npm install --save-dev husky
```

## Edit package.json to include husky

```json
"husky": {
  "hooks": {
      "pre-commit": "pretty-quick — staged && ng lint"
  }
},
```

## Edit tslint.json

Change first line of tslint.json from

```json
"extends": "tslint:recommended",
```

to

```json
"extends": ["tslint:recommended", "tslint-angular", "tslint-config-prettier"],
```

## View your project through a browser

```bash
npm start
```

The app will be viewable at [http://localhost:4200](http://localhost:4200)

## Updating your NPM packages and Angular to latest versions

```bash
npm install -g npm-check-updates
ncu -u --packageFile package.json
npm update
npm install
```

## Uploading your project to be viewed as a website publicly

This works only with git projects uploaded via Github

```bash
npm install -g angular-cli-ghpages
```

Then edit package.json and add a new entry to the `scripts` section

```json
"deploy": "ng build --prod --base-href https://<yourgithubusername>.github.io/<yourprojectname>/ && ngh --dir=dist/<yourprojectname>"
```

To run the deploy

```bash
npm run deploy
```
