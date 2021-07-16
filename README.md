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
    "typescript.updateImportsOnFileMove.enabled": "always",
    "workbench.iconTheme": "material-icon-theme",
    // Terminal Settings
    "terminal.integrated.defaultProfile.windows": "Git Bash",
    // Peacock Settings
    "peacock.favoriteColors": [
      {
        "name": "Angular Red",
        "value": "#b52e31"
      },
      {
        "name": "Mandalorian Blue",
        "value": "#1857a4"
      },
      {
        "name": "Sky Purple",
        "value": "#a833ff"
      }
    ],
    // Javascript Settings
    "js/ts.implicitProjectConfig.experimentalDecorators": true,
    // ESLint Settings
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
    "prettier",
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
    "simple-import-sort/imports": "error"
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
    "selector-type-no-unknown": null,
    "selector-pseudo-element-no-unknown": null,
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
npm install --save bootstrap jquery @popperjs/core font-awesome
```

Edit angular.json to include Font Awesome and Bootstrap (Note: this will need to be added in two places in this file)
```json
"styles": [
  "./node_modules/font-awesome/css/font-awesome.min.css",
  "./node_modules/bootstrap/dist/css/bootstrap.min.css",
  "src/assets/scss/styles.scss"
],
"scripts": [
  "./node_modules/jquery/dist/jquery.slim.min.js",
  "./node_modules/@popperjs/core/dist/umd/popper.min.js",
  "./node_modules/bootstrap/dist/js/bootstrap.min.js"
]
```

## Configure project
* Edit tsconfig.json to support smart paths and node imports. Between module and lib, add:
```json
"paths": {
  "@app/*": ["src/app/*"],
  "@assets/*": ["src/assets/*"],
  "@environments/*": ["src/environments/*"]
},
"typeRoots": ["node_modules/@types"],
```
* Also in tsconfig.json enable strictTemplates for all language features
```json
"angularCompilerOptions": {
  "strictTemplates": true
}
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

* After you move your styles.scss and app.component.scss files to /assets/scss, Edit app.component.ts
``` typescript
styleUrls: ['../assets/scss/app.component.scss']
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
import { AppRoutingModule } from './app-routing.module';
import { AppComponent } from './app.component';

@NgModule({
  declarations: [AppComponent],
  imports: [
    // angular
    BrowserModule,
    BrowserAnimationsModule,

    // all feature modules not lazy loaded

    // core
    CoreModule,

    // app
    AppRoutingModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule {}
```
* Create a Homepage
```bash
ng g m modules/home
ng g c modules/home/pages/home --module='modules\home\home.module.ts'
```

* Modify the app-routing.module.ts to load in the new feature
```typescript
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';

import { HomeComponent } from './modules/home/pages/home/home.component';

const routes: Routes = [{ path: '', component: HomeComponent }];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule {}
```

* Modify the new feature module `home.module.ts` to add in the Shared Module, make sure the import statement is at the top of the file
```typescript
  imports: [
    CommonModule,
    SharedModule
  ]
```

* Create Homepage Content
```html
<main class="flex-shrink-0">
  <div class="container">
    <h1 class="mt-5">Home</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
      magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
      consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
      Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  </div>
</main>
```

* Any feature you create within the application (other than home page) should be set up to be lazy loaded. The example below will be for creating an `ABOUT` feature with a default home page for this new section. Just replace the word `about` for the name of your feature.
```bash
ng g m modules/about --routing
ng g c modules/about/pages/about-home --module='modules\about\about.module.ts'
```

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

## Optional - Adding Angular Material
```bash
ng add @angular/material
```

Choose a pre-built theme. - `Deep Purple - Amber` 

Choose wheter to apply global typography styles. - `Yes`

Choose to set up browser animations. - `Yes`


* Create material.module.ts at /shared/material/material.module.ts

```typescript
import { CommonModule } from '@angular/common';
import { NgModule } from '@angular/core';
import { MatAutocompleteModule } from '@angular/material/autocomplete';
import { MatBadgeModule } from '@angular/material/badge';
import { MatBottomSheetModule } from '@angular/material/bottom-sheet';
import { MatButtonModule } from '@angular/material/button';
import { MatButtonToggleModule } from '@angular/material/button-toggle';
import { MatCardModule } from '@angular/material/card';
import { MatCheckboxModule } from '@angular/material/checkbox';
import { MatChipsModule } from '@angular/material/chips';
import { MatRippleModule } from '@angular/material/core';
import { MatDatepickerModule } from '@angular/material/datepicker';
import { MatDialogModule } from '@angular/material/dialog';
import { MatDividerModule } from '@angular/material/divider';
import { MatExpansionModule } from '@angular/material/expansion';
import { MatFormFieldModule } from '@angular/material/form-field';
import { MatGridListModule } from '@angular/material/grid-list';
import { MatIconModule } from '@angular/material/icon';
import { MatInputModule } from '@angular/material/input';
import { MatListModule } from '@angular/material/list';
import { MatMenuModule } from '@angular/material/menu';
import { MatPaginatorModule } from '@angular/material/paginator';
import { MatProgressBarModule } from '@angular/material/progress-bar';
import { MatProgressSpinnerModule } from '@angular/material/progress-spinner';
import { MatRadioModule } from '@angular/material/radio';
import { MatSelectModule } from '@angular/material/select';
import { MatSidenavModule } from '@angular/material/sidenav';
import { MatSlideToggleModule } from '@angular/material/slide-toggle';
import { MatSliderModule } from '@angular/material/slider';
import { MatSnackBarModule } from '@angular/material/snack-bar';
import { MatSortModule } from '@angular/material/sort';
import { MatStepperModule } from '@angular/material/stepper';
import { MatTableModule } from '@angular/material/table';
import { MatTabsModule } from '@angular/material/tabs';
import { MatToolbarModule } from '@angular/material/toolbar';
import { MatTooltipModule } from '@angular/material/tooltip';
import { MatTreeModule } from '@angular/material/tree';

@NgModule({
  declarations: [],
  imports: [
    CommonModule,
    // Material Form Controls
    MatAutocompleteModule,
    MatCheckboxModule,
    MatDatepickerModule,
    MatFormFieldModule,
    MatInputModule,
    MatRadioModule,
    MatSelectModule,
    MatSliderModule,
    MatSlideToggleModule,
    // Material Navigation
    MatMenuModule,
    MatSidenavModule,
    MatToolbarModule,
    // Material Layout
    MatCardModule,
    MatDividerModule,
    MatExpansionModule,
    MatGridListModule,
    MatListModule,
    MatStepperModule,
    MatTabsModule,
    MatTreeModule,
    // Material Buttons & Indicators
    MatButtonModule,
    MatButtonToggleModule,
    MatBadgeModule,
    MatChipsModule,
    MatIconModule,
    MatProgressSpinnerModule,
    MatProgressBarModule,
    MatRippleModule,
    // Material Popups & Modals
    MatBottomSheetModule,
    MatDialogModule,
    MatSnackBarModule,
    MatTooltipModule,
    // Material Data tables
    MatPaginatorModule,
    MatSortModule,
    MatTableModule
  ],
  exports: [
    // Material Form Controls
    MatAutocompleteModule,
    MatCheckboxModule,
    MatDatepickerModule,
    MatFormFieldModule,
    MatInputModule,
    MatRadioModule,
    MatSelectModule,
    MatSliderModule,
    MatSlideToggleModule,
    // Material Navigation
    MatMenuModule,
    MatSidenavModule,
    MatToolbarModule,
    // Material Layout
    MatCardModule,
    MatDividerModule,
    MatExpansionModule,
    MatGridListModule,
    MatListModule,
    MatStepperModule,
    MatTabsModule,
    MatTreeModule,
    // Material Buttons & Indicators
    MatButtonModule,
    MatButtonToggleModule,
    MatBadgeModule,
    MatChipsModule,
    MatIconModule,
    MatProgressSpinnerModule,
    MatProgressBarModule,
    MatRippleModule,
    // Material Popups & Modals
    MatBottomSheetModule,
    MatDialogModule,
    MatSnackBarModule,
    MatTooltipModule,
    // Material Data tables
    MatPaginatorModule,
    MatSortModule,
    MatTableModule
  ]
})
export class MaterialModule {}
```
* Edit shared.module.ts. Add MaterialModule in imports and exports section
```typescript
@NgModule({
  // modules
  imports: [CommonModule, ReactiveFormsModule, MaterialModule],
  // components, directives, pipes
  declarations: [],
  // modules & components, directives, pipes
  exports: [CommonModule, ReactiveFormsModule, MaterialModule]
})
```

## Optional - Create Header and Footer Component
* Create Component
```bash
ng g c core/header
ng g c core/footer
```

* Modify core.module.ts to add HeaderComponent and FooterComponent to declarations and export secttions
```typescript
@NgModule({
  // modules
  imports: [CommonModule, HttpClientModule, RouterModule],
  // header, footer
  declarations: [HeaderComponent, FooterComponent],
  // guards, interceptors, services
  providers: [],
  // header, footer
  exports: [HeaderComponent, FooterComponent]
})
```

* Edit index.html and change body
```html
<body class="container pt-3 h-100">
  <app-root class="d-flex flex-column h-100"></app-root>
</body>
```

* Edit header.html
```html
<header>
  <nav class="navbar navbar-expand-md navbar-dark fixed-top bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Brand Name</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarCollapse"
        aria-controls="navbarCollapse" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarCollapse">
        <ul class="navbar-nav me-auto mb-2 mb-md-0">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
          </li>
        </ul>
        <form class="d-flex">
          <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-outline-success" type="submit">Search</button>
        </form>
      </div>
    </div>
  </nav>
</header>
```

* Edit footer.component.html
```html
<footer class="footer py-3 bg-dark">
  <div class="container">
    <span class="text-muted">Place sticky footer content here.</span>
  </div>
</footer>
```

* Edit app.component.html
```html
<app-header></app-header>
<router-outlet></router-outlet>
<app-footer class="mt-auto"></app-footer>
```

* Edit styles.css to allow room for sticky footer
```css
main {
  margin-bottom: 60px;
}
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
"deploy": "ng build --configuration production --base-href https://<yourgithubusername>.github.io/<yourprojectname>/ && ngh --dir=dist/<yourprojectname>"
```

To run the deploy

```bash
npm run deploy
```
