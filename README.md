# Angular Setup

## Programs to Download

- [Git w/ Gitbash](https://git-scm.com/downloads)
- [Visual Studio Code](https://code.visualstudio.com/Download)
- [Node with NPM](https://nodejs.org/en)

## Install Node

Let's check to see if you have Node installed. Open up command prompt and type `node -v`

You should see something like `v12.1.0`

If you don't have node then let's [install it](https://nodejs.org/en/download)

## NPM

NPM is the default package manager for the JavaScript runtime environment Node.js. NPM automatically comes with the node.js install

See what version you are on `npm -v`

## Terminal

For Mac users, you should already have terminal installed. Windows users, I'd recommend [GITbash](http://git-scm.com). This is preferable than using Windows command prompt.

## Visual Studio Code Extensions

VSC comes with many extensions to make editing code easier. Below is a list of extensions I'd recommend on adding to it. Click on the extensions tab in your editor to begin searching and installing.

**Install**

- [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template)
- [Angular Snippets](https://marketplace.visualstudio.com/items?itemName=johnpapa.Angular2)
- [Bootstrap 5 & Font Awesome Snippets](https://marketplace.visualstudio.com/items?itemName=HansUXdev.bootstrap5-snippets)
- [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [JSON to Reactive Form](https://marketplace.visualstudio.com/items?itemName=jawahargopal.json-2-reactive-form)
- [JSON to TS](https://marketplace.visualstudio.com/items?itemName=MariusAlchimavicius.json-to-ts)
- [Live Frame](https://marketplace.visualstudio.com/items?itemName=jevakallio.vscode-live-frame)
- [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)
- [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
- [Mintlify Doc Writer for Python, JavaScript, TypeScript, C++, PHP, Java, C#, Ruby & more](https://marketplace.visualstudio.com/items?itemName=mintlify.document)
- [Nx Console](https://marketplace.visualstudio.com/items?itemName=nrwl.angular-console)
- [Peacock](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock)
- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Snipped](https://marketplace.visualstudio.com/items?itemName=JeffersonLicet.snipped)
- [Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint)
- [Thunder Client](https://marketplace.visualstudio.com/items?itemName=rangav.vscode-thunder-client)
- [Version Lens](https://marketplace.visualstudio.com/items?itemName=pflannery.vscode-versionlens)
- [vscode-json](https://marketplace.visualstudio.com/items?itemName=andyyaldoo.vscode-json)
- [Git Extension Pack](https://marketplace.visualstudio.com/items?itemName=donjayamanne.git-extension-pack) - This automatically adds following extensions:
  - [Git History](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)
  - [gitignore](https://marketplace.visualstudio.com/items?itemName=codezombiech.gitignore)
  - [GitLens - Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
  - [Open in GitHub, Bitbucket, Gitlab, VisualStudio.com](https://marketplace.visualstudio.com/items?itemName=ziyasal.vscode-open-in-github)
  - [Project Manager](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)


## VS Code Settings (settings.json)

You can find this file in VS Code, by going to `File>Preferences>Settings`. In the upper right corder you'll see an icon that says `Open Settings (JSON)` and it'll open your settings.json file. My settings.json looks like:

```json
{
  // Basic Settings
  "explorer.compactFolders": false,
  "typescript.updateImportsOnFileMove.enabled": "always",
  "workbench.iconTheme": "material-icon-theme",
  "editor.bracketPairColorization.enabled": true,
  "git.autofetch": true,
  "versionlens.suggestions.showOnStartup": true,
  "docwriter.hotkey.windows": "Alt + .",
  "docwriter.hotkey.mac": "⌥ + .",

  // Live Frame settings
  "liveFrame.url": "http://localhost:4200",
  "liveFrame.title": "Local Development",
  "liveFrame.pane": "Beside",

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
  "javascript.updateImportsOnFileMove.enabled": "always",

  // ESLint Settings
  "eslint.format.enable": true,
  "eslint.validate": [
    "javascript",
    "typescript"
  ],

  // Stylelint Settings
  "css.validate": false,
  "less.validate": false,
  "scss.validate": false,
  "stylelint.validate": ["css", "scss", "less"],

  // Individual File Settings
  "[javascript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
    "editor.codeActionsOnSave": {
      "source.fixAll": true
    }
  },
  "[typescript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
    "editor.codeActionsOnSave": {
      "source.fixAll": true
    }
  },
  "[html]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.codeActionsOnSave": {
      "source.fixAll": true
    }
  },
  "[json]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.codeActionsOnSave": {
      "source.fixAll": true
    }
  },
  "[scss]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.codeActionsOnSave": {
      "source.fixAll": true
    }
  },
  "[css]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.codeActionsOnSave": {
      "source.fixAll": true
    }
  }
  
}
```

## Install Angular

```bash
npm install -g @angular/cli
```

## Create a new project

This will install a new Angular project with SCSS for styling instead of the default CSS. It will also add Angular routing to the project.

```bash
ng new nameofproject --style=scss --routing
```
## Add linting to project
Linting is the process of running a program that will check code for potential errors prior to check in.
### Prettier
```bash
npm i -D prettier
touch .prettierrc.json
touch .prettierignore
```

Edit prettier settings (.prettierrc.json)
```json
{
  "printWidth": 100,
  "singleQuote": true,
  "trailingComma": "none",
  "bracketSameLine": true,
  "htmlWhitespaceSensitivity": "ignore",
  "endOfLine": "auto"
}
```

Edit Prettier ignore file (.prettierignore)
```json
dist
package-lock.json
package.json
```

Edit package.json and add Prettier in scripts section
```json
"prettier": "npx prettier \"src/**/*.{html,json}\" --write"
```

###ESLint
```bash
ng add @angular-eslint/schematics
npm i -D eslint-config-prettier eslint-plugin-prettier eslint-plugin-simple-import-sort
touch .eslintignore
```

Modify Eslint settings (eslintrc.json)
```json
{
  "env": {
    "browser": true,
    "jasmine": true,
    "node": true
  },
  "root": true,
  "ignorePatterns": ["projects/**/*"],
  "overrides": [
    {
      "files": ["*.ts"],
      "parserOptions": {
        "project": ["tsconfig.json"],
        "createDefaultProgram": true
      },
      "plugins": ["simple-import-sort"],
      "extends": [
        "eslint:recommended",
        "plugin:@angular-eslint/recommended",
        "plugin:@angular-eslint/template/process-inline-templates",
        "plugin:prettier/recommended"
      ],
      "rules": {
        "@angular-eslint/directive-selector": [
          "error",
          {
            "type": "attribute",
            "prefix": "app",
            "style": "camelCase"
          }
        ],
        "@angular-eslint/component-selector": [
          "error",
          {
            "type": "element",
            "prefix": "app",
            "style": "kebab-case"
          }
        ],
        "simple-import-sort/imports": "warn",
        "prettier/prettier": "warn",
        "no-unused-vars": "off",
        "linebreak-style": 0
      }
    },
    {
      "files": ["*.html"],
      "extends": ["plugin:@angular-eslint/template/recommended"],
      "rules": {}
    }
  ]
}
```

Edit ESLint ignore file (.eslintignore)
```json
dist
karma.conf.js
```

Edit package.json and add ESLint in scripts section
```json
"eslint": "npx eslint \"src/**/*.{js,ts}\" --fix"
```

### Stylelint
```bash
npm i -D stylelint stylelint-config-prettier stylelint-config-standard-scss
touch .stylelintrc.json
touch .styelintignore
```

Edit Styelint settings (.stylelintrc.json)
```json
{
  "extends": ["stylelint-config-standard-scss", "stylelint-config-prettier"],
  "rules": {
    "no-empty-source": null
  }
}
```

Edit Stylelint ignore file (.styelintignore)
```json
**/*.js
**/*.ts
**/*.json
```

Edit package.json and add Prettier in scripts section
```json
"stylelint": "npx stylelint \"src/**/*.{css,scss}\" --fix"
```

### Husky and Lint Staged
```bash
npm i -D husky
npx husky install
npm i -D lint-staged
npx husky add .husky/pre-commit "npx lint-staged"
```

Edit package.json to add Husky in scripts section
```json
"prepare": "husky install"
```

Also add new section to package.json for lint-staged
```json
"lint-staged": {
  "*.{html,json}": "prettier --write",
  "*.{js,ts}": "eslint --fix",
  "*.{css,scss}": "stylelint --fix"
},
```


## Add Bootstrap with PopperJs

```bash
npm install --save bootstrap @popperjs/core
```

Edit angular.json to include Bootstrap (Note: this will need to be added in two places in this file)
```json
"styles": [
  "./node_modules/bootstrap/dist/css/bootstrap.min.css",
  "src/assets/scss/styles.scss"
],
"scripts": [
  "./node_modules/@popperjs/core/dist/umd/popper.min.js",
  "./node_modules/bootstrap/dist/js/bootstrap.min.js"
]
```

## Configure project
Edit tsconfig.json to support smart paths and node imports. After "lib" section, add:
```json
"paths": {
  "@app/*": ["src/app/*"],
  "@assets/*": ["src/assets/*"],
  "@environments/*": ["src/environments/*"]
},
"typeRoots": ["node_modules/@types"]
```

Create the folder modules for your project
```bash
ng g m core
ng g m shared
```

Create the folder structure per the below diagram
```
|-- app
    |-- core
        |-- animations
            |-- *.animations.ts
        |-- components
            |-- navbar
                |-- navbar.component.html|scss|ts
            |-- page-not-found
                |-- page-not-found.component.html|scss|ts
        |-- guards
            |-- *.guard.ts
        |-- interceptors
            |-- *.interceptor.ts
        |-- models
            |-- *.model.ts
        |-- services
            |-- *.service.ts
        |-- utils
            |-- common-functions.ts
        |-- core.module.ts
    |-- features (different name for each feature in the application)
        |-- components
            |-- scoped-component
                |-- *.component.html|scss|ts
        |-- pages
            |-- page (different name for each page in each feature)
              |-- page.component.ts|html|scss
        |-- models
            |-- scoped-model
                |-- *.model.ts
        |-- services
            |-- scoped-service.ts
        |-- feature.module.ts
        |-- feature-routing.module.ts (only if lazy loading)
    |-- shared
        |-- components
            |-- component (different name for each component)
                |-- component.component.ts|html|scss|spec.ts
        |-- directives
            |-- *.directive.ts
        |-- pipes
            |-- *.pipe.ts
        |-- shared.module.ts
|-- styles.scss
|-- styles
    |-- *.scss
|-- assets
    |-- i18n
        |-- language.json (different name for each language)
    |-- images
        |-- *.svg|jpg|gif|png
    |-- static
        |-- *.json
    |-- icons
        |-- *.svg
```



Edit core.module.ts
``` typescript
import { CommonModule } from '@angular/common';
import { HttpClientModule } from '@angular/common/http';
import { NgModule, Optional, SkipSelf } from '@angular/core';
import { RouterModule } from '@angular/router';

@NgModule({
  // modules
  imports: [CommonModule, HttpClientModule, RouterModule],
  // core components
  declarations: [],
  // guards, interceptors, services
  providers: [],
  // core components
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
ng g m features/home
ng g c features/home/pages/home --module='features\home\home.module.ts'
```

* Edit app.module.ts to add in HomeModule since it won't be lazy loaded
```typescript
  // all feature modules not lazy loaded
  HomeModule,
```

* Modify the app-routing.module.ts to load in the new feature
```typescript
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';

import { HomeComponent } from './features/home/pages/home/home.component';

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

## Optional - Adding Angular Material
```bash
ng add @angular/material
```

Choose a theme. - `Custom`

Choose wheter to apply global typography styles. - `Yes`

Choose to set up browser animations. - `Include and enable animations`


* Create material.module.ts at /shared/material.module.ts

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
Edit shared.module.ts. Add MaterialModule in imports and exports section
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

Update app.component.html to at least use the router. Long term this be can changed to include a navigation bar, header, and footer.
```html
<router-outlet></router-outlet>
```


* Create Homepage Content at home.component.html
```html
<section>
  <div class="container-fluid">
    <div class="row"><h1>Home</h1></div>
    <div class="row">
      <div class="col-md-6 p-3">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
          ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation
          ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
          sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
          est laborum.
        </p>
      </div>
      <div class="col-md-6 p-3">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
          ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation
          ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
          sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
          est laborum.
        </p>
      </div>
    </div>
  </div>
</section>
```

* Any feature you create within the application (other than home page) should be set up to be lazy loaded. The example below will be for creating an `ABOUT` feature with a default home page for this new section. Just replace the word `about` for the name of your feature.
```bash
ng g m features/about --routing
ng g c features/about/pages/about --module='features\about\about.module.ts'
```

* Modify the app-routing.module.ts to lazy load in the new feature
```typescript
const routes: Routes = [
{ path: 'about', loadChildren: () => import('./features/about/about.module').then(m => m.AboutModule) }
];
@NgModule({
  imports: [
    RouterModule.forRoot(routes, { preloadingStrategy: PreloadAllModules })
  ],
  exports: [RouterModule]
})
export class AppRoutingModule {}
```

* Modify the new feature module `about.module.ts` to add in the Shared Module
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

## Optional - Create custom theme
If you choose to not do this, the Material theme of indigo and pink will be chosen for you.
* Go to [Material Theme & Palette Generator](http://mcg.mbitson.com/)
* Click on the Plus Icon to `Add Palette` twice (should be three total)
* Name first palette `primary`, second `accent`, third `warn`
* Change the colors to whatever you want
* Click on the down arrow icon, which is `Copy AngularJS code / Export`.
* Change Output format to `Angular JS 2 (Material 2)`
* Copy code and paste it in `styles.scss` directly after `@include mat.core;` on the next line.
* Stylelint will complain about several linting errors, here's how to fix them: 
  * Add stylelint exception rules to top of file
  ```css
  /* stylelint-disable scss/dollar-variable-pattern */
  ```
  * Some of the hex codes for colors will need to be shortened depending on what colors you used. Stylelint should auto format these after you save the file
* Add in three new css selectors to reuse the colors throughout the application. Place these after the body selector
```css
.primary-color {
  color: mat.get-color-from-palette($ProjectName-primary);
}

.primary-background {
  background-color: mat.get-color-from-palette($ProjectName-primary);
  color: #fff;
}

.accent-color {
  color: mat.get-color-from-palette($ProjectName-accent);
}

.accent-background {
  background-color: mat.get-color-from-palette($ProjectName-primary);
  color: #000;
}

.warn-color {
  color: mat.get-color-from-palette($ProjectName-warn);
}
```



## Optional - Add in Resposnive Sidebar Menu

* Edit core.module.ts to add in required Material Modules
```typescript
imports: [
  ...
  MatToolBarModule,
  MatSideNavModule,
  MatButtonModule,
  MatIconModule
]
exports: [
  ...
  MatToolBarModule,
  MatSideNavModule,
  MatButtonModule,
  MatIconModule
]
```

* Edit app.component.html
```html
<mat-toolbar class="primary-background">
  <button mat-icon-button *ngIf="sidenav.mode === 'over'" (click)="sidenav.toggle()">
    <mat-icon *ngIf="!sidenav.opened">menu</mat-icon>
    <mat-icon *ngIf="sidenav.opened">close</mat-icon>
  </button>
  Application Name
</mat-toolbar>
<mat-sidenav-container>
  <mat-sidenav #sidenav="matSidenav" class="mat-elevation-z8">
    <div>
      <button mat-button class="menu-button" color="primary">
        <mat-icon>home</mat-icon>
        <span>Home</span>
      </button>
    </div>
    <div>
      <button mat-button class="menu-button" color="primary">
        <mat-icon>person</mat-icon>
        <span>Profile</span>
      </button>
    </div>
    <div>
      <button mat-button class="menu-button" color="primary">
        <mat-icon>info</mat-icon>
        <span>About</span>
      </button>
    </div>
  </mat-sidenav>
  <mat-sidenav-content>
    <div class="content mat-elevation-z8"><router-outlet></router-outlet></div>
  </mat-sidenav-content>
</mat-sidenav-container>

```

* Edit app.component.ts
```typescript
import { BreakpointObserver } from '@angular/cdk/layout';
import { AfterViewInit, Component, ViewChild } from '@angular/core';
import { MatSidenav } from '@angular/material/sidenav';
import { delay } from 'rxjs/operators';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent implements AfterViewInit {
  @ViewChild(MatSidenav)
  sidenav!: MatSidenav;

  constructor(private observer: BreakpointObserver) {}

  ngAfterViewInit() {
    this.observer
      .observe(['(max-width: 768px)'])
      .pipe(delay(1))
      .subscribe((res) => {
        if (res.matches) {
          this.sidenav.mode = 'over';
          this.sidenav.close();
        } else {
          this.sidenav.mode = 'side';
          this.sidenav.open();
        }
      });
  }
}
```

* Edit app.component.scss
```css
mat-sidenav {
  width: 200px;
  padding: 8px 8px 12px;
}

.content {
  min-height: calc(100vh - 64px);
  padding: 20px;
}

mat-sidenav-container {
  min-height: calc(100vh - 64px);
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
