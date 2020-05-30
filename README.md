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
  - [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template)
  - [Angular Snippets](https://marketplace.visualstudio.com/items?itemName=johnpapa.Angular2)
  - [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)
  - [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge)
  - [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
  - [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
  - [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
  - [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script)
  - [Nx Console](https://marketplace.visualstudio.com/items?itemName=nrwl.angular-console)
  - [Peacock](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock)
  - [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
  - [Winter is Coming Theme](https://marketplace.visualstudio.com/items?itemName=johnpapa.winteriscoming)
- [Git Extension Pack](https://marketplace.visualstudio.com/items?itemName=donjayamanne.git-extension-pack) - This automatically adds following extensions:
  - [Git History](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)
  - [gitignore](https://marketplace.visualstudio.com/items?itemName=codezombiech.gitignore)
  - [GitLens - Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
  - [Open in GitHub, Bitbucket, Gitlab, VisualStudio.com](https://marketplace.visualstudio.com/items?itemName=ziyasal.vscode-open-in-github)
  - [Project Manager](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)
- [Bootstrap 4, Font awesome 4, Font Awesome 5 Free & Pro snippets](https://marketplace.visualstudio.com/items?itemName=thekalinga.bootstrap4-vscode)
- [JSON to Reactive Form](https://marketplace.visualstudio.com/items?itemName=jawahargopal.json-2-reactive-form)
- [stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint)

## VS Code Settings (settings.json)

You can find this file in VS Code, by going to `File>Preferences>Settings`. In the upper right corder you'll see an icon that says `Open Settings (JSON)` and it'll open your settings.json file. My settings.json looks like:

```json
{
  "git.autofetch": true,
  // Terminal Settings
  "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
  "typescript.updateImportsOnFileMove.enabled": "always",
  "workbench.iconTheme": "material-icon-theme",
  "workbench.colorTheme": "Winter is Coming (Dark Blue)",
  // Peacock Settings
  "peacock.favoriteColors": [
    {
      "name": "Angular Red",
      "value": "#b52e31"
    },
    {
      "name": "Mandalorian Blue",
      "value": "#1857a4"
    }
  ],
  // ESLint Settings
  "eslint.enable": true,
  "eslint.format.enable": true,
  "eslint.validate": [
    "javascript",
    "typescript"
  ],
  "eslint.alwaysShowStatus": true,
  // Individual File Settings
  "[javascript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
    }
  },
  "[typescript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
    },
  },
  "[html]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "vscode.html-language-features",
    "editor.codeActionsOnSave": {
      "source.fixAll.stylelint": true
    }
  },
  "[scss]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.codeActionsOnSave": {
      "source.fixAll.stylelint": true
    }
  },
  "[css]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.codeActionsOnSave": {
      "source.fixAll.stylelint": true
    }
  },
  "[json]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
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

## Add Dev Dependencies for Prettier, ESLint, and Stylelint
```bash
# Install ESLint
npm install --save-dev eslint

# Install additional plugins
npm install --save-dev @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-plugin-prettier eslint-plugin-simple-import-sort

# Install Prettier and Prettier-ESLint dependencies
npm install --save-dev prettier prettier-eslint eslint-config-prettier eslint-plugin-prettier

# Install Stylelint and Stylelint dependencies
npm install --save-dev stylelint stylelint-config-prettier stylelint-config-standard
```

## Add prettier setting files

Navigate into your new project directory

```bash
touch .prettierrc
touch .prettierignore
```

### Prettier settings (.prettierrc)

```json
{
  "singleQuote": true,
  "jsxBracketSameLine": true,
  "trailingComma": "none",
  "endOfLine": "auto"
}
```

### Prettier ignore file (.prettierignore)

```json
dist
package.json
package-lock.json
```

## Add ESLint setting files

Navigate into your new project directory

```bash
touch .eslintrc
touch .eslintignore
```

### ESLint settings (.eslintrc)

```json
{
  "env": {
    "browser": true,
    "amd": true,
    "node": true
  },
  "parser": "@typescript-eslint/parser",
  "plugins": ["simple-import-sort", "@typescript-eslint"],
  "extends": [
    "eslint:recommended",
    "plugin:@typescript-eslint/eslint-recommended",
    "plugin:@typescript-eslint/recommended",
    "prettier/@typescript-eslint",
    "plugin:prettier/recommended"
  ],
  "parserOptions": {
    "ecmaVersion": 2020, // Allows for the parsing of modern ECMAScript features
    "sourceType": "module" // Allows for the use of imports
  },
  "rules": {
    "@typescript-eslint/no-explicit-any": "off",
    "@typescript-eslint/explicit-function-return-type": "off",
    "@typescript-eslint/no-empty-function": "off",
    "@typescript-eslint/no-var-requires": 0,
    "simple-import-sort/sort": "error"
  }
}
```

### ESLint ignore file (.eslintignore)

```json
!**/.eslintrc*
node_modules*
e2e
dist
*.svg
*.ico
*.json
.gitignore
*.md
*.log
*.lock
```

## Add Stylelint setting files

Navigate into your new project directory

```bash
touch .stylelintrc
touch .stylelintignore
```

### Styelint settings (.stylelintrc)

```json
{
  "extends": [
    "stylelint-config-standard",
    "stylelint-config-prettier"
  ],
  "rules": {
    "selector-type-no-unknown": [true, {
      ignoreTypes: [
        "router-outlet"
      ]
    }],
    "no-empty-source": null
  }
}
```

### Stylelint ignore file (.stylelintignore)

```json
**/*.js
**/*.ts
**/*.json
```

## Add Font Awesome and Bootstrap

```bash
npm install --save bootstrap jquery popper.js font-awesome
```

Edit angular.json to include Font Awesome and Bootstrap
```json
"styles": [
  "node_modules/font-awesome/css/font-awesome.min.css",
  "node_modules/bootstrap/dist/css/bootstrap.min.css",
  "src/assets/scss/styles.scss"
],
"scripts": [
  "node_modules/jquery/dist/jquery.slim.min.js",
  "node_modules/popper.js/dist/umd/popper.min.js",
  "node_modules/bootstrap/dist/js/bootstrap.min.js"
]
```

## Configure project
* Edit tsconfig.json to support smart paths and node imports. Between target and lib, add:
```json
"paths": {
  "@app/*": ["src/app/*"],
  "@assets/*": ["src/assets/*"],
  "@environments/*": ["src/environments/*"]
},
"typeRoots": ["node_modules/@types"],
```
* Edit tsconfig.app.json, add *node* to types
```json
"types": ["node"]
```

* Create the folder modules for your project
```bash
ng g m core
ng g m shared
```

* Create the folder structure per the below diagram
```
|-- app
    |-- modules
        |-- feature (different name for each feature in the application)
            |-- pages
                |-- page (different name for each page in each feature)
                  |-- page.component.ts|html|scss|spec.ts
            |-- feature.module.ts
            |-- feature-routing.module.ts (only if lazy loading)
    
    |-- core
        |-- animations
            |-- *.animations.ts
        |-- footer
            |-- footer.component.ts|html|scss|spec.ts
        |-- guards
            |-- *.guard.ts
        |-- header
            |-- header.component.ts|html|scss|spec.ts
        |-- interceptors
            |-- *.interceptor.ts
        |-- services
            |-- *.service.ts|spec.ts
        |-- core.module.ts
    |-- shared
        |-- components
            |-- component (different name for each component)
                |-- component.component.ts|html|scss|spec.ts
        |-- directives
            |-- *.directive.ts
        |-- pipes
            |-- *.pipe.ts
        |-- models
            |-- *.model.ts
|-- assets
    |-- images
    |-- scss
        |-- *.scss
```

* Edit core.module.ts
``` typescript
import { CommonModule } from '@angular/common';
import { HttpClientModule } from '@angular/common/http';
import { NgModule, Optional, SkipSelf } from '@angular/core';
import { RouterModule } from '@angular/router';

@NgModule({
  // modules
  imports: [CommonModule, HttpClientModule, RouterModule],
  // header, footer
  declarations: [],
  // guards, interceptors, services
  providers: [],
  // header, footer
  exports: []
})
export class CoreModule {
  constructor(@Optional() @SkipSelf() parentModule: CoreModule) {
    if (parentModule) {
      throw new Error('CoreModule is already loaded. Import only in AppModule');
    }
  }
}
```

* Edit shared.module.ts
``` typescript
import { CommonModule } from '@angular/common';
import { NgModule } from '@angular/core';
import { ReactiveFormsModule } from '@angular/forms';

@NgModule({
  // modules
  imports: [
    CommonModule,
    ReactiveFormsModule
  ],
  // components, directives, pipes
  declarations: [],
  // modules & components, directives, pipes
  exports: [
    CommonModule,
    ReactiveFormsModule
  ]
})
export class SharedModule {}
```

* Edit app.module.ts to support this new structure
```typescript
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
import { CoreModule } from '@app/core/core.module';
import { SharedModule } from '@app/shared/shared.module';
import { AppRoutingModule } from './app-routing.module';
import { AppComponent } from './app.component';

@NgModule({
  declarations: [AppComponent],
  imports: [
    // angular
    BrowserModule,
    BrowserAnimationsModule,

    // all feature modules not lazy loaded

    // core & shared
    CoreModule,
    SharedModule,

    // app
    AppRoutingModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule {}
```

* Any feature you create within the application should be set up to be lazy loaded. The example below will be for creating an `ABOUT` feature with a default home page for this new section. Just replace the word `about` for the name of your feature.
```bash
ng g m modules/about --routing
ng g c modules/about/pages/about-home --module='modules\about\about.module.ts'
````

* Modify the app-routing.module.ts to lazy load in the new feature
```typescript
const routes: Routes = [
{ path: 'about', loadChildren: () => import('./modules/about/about.module').then(m => m.AboutModule) }
];
@NgModule({
  imports: [
    RouterModule.forRoot(routes, { preloadingStrategy: PreloadAllModules })
  ],
  exports: [RouterModule]
})
export class AppRoutingModule {}
```

* Modify the new feature module `about.module.ts` to add in the Shared Module, make sure the import statement is at the top of the file
```typescript
  imports: [
    CommonModule,
    AboutRoutingModule,
    SharedModule
  ]
```

* Modify the new feature routing module `about-routing.module.ts` to add in the home page of the `about` section
```typescript
const routes: Routes = [{ path: '', component: AboutHomeComponent }];
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
