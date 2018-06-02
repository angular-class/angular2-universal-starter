<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/1016365/10639063/138338bc-7806-11e5-8057-d34c75f3cafc.png" alt="Universal Angular" height="320"/>
</p>

# Angular Universal Starter
> Server-Side Rendering for Angular

A minimal Angular starter for Universal JavaScript using the [Angular CLI](/angular/angular-cli)
If you're looking for the Angular Universal repo go to [**angular/universal**](/angular/universal)  

## Getting Started

This demo is built following the [Angular-CLI Wiki guide](/angular/angular-cli/wiki/stories-universal-rendering)

We're utilizing packages from the [Angular Universal @nguniversal](/angular/universal) repo, such as [ng-module-map-ngfactory-loader](/angular/universal/modules/module-map-ngfactory-loader) to enable Lazy Loading.

---

### Build Time Prerendering Vs. Server Side Rendering(ssr)
This repo demonstrates the use of 2 different forms of Server Side Rendering.

**Prerender** 
* Happens at build time
* Renders your application and replaces the dist index.html with a version rendered at the route `/`.

**Server-Side Rendering(ssr)**
* Happens at runtime
* Uses `ngExpressEngine` to render your application on the fly at the requested url.

---

### Installation
* `npm install` or `yarn`

### Development (Client-side only rendering)
* run `npm run start` which will start `ng serve`

### Production (also for testing SSR/Pre-rendering locally)
**`npm run build:ssr && npm run serve:ssr`** - Compiles your application and spins up a Node Express to serve your Universal application on `http://localhost:4000`.

**`npm run build:prerender && npm run serve:prerender`** - Compiles your application and prerenders your applications files, spinning up a demo http-server so you can view it on `http://localhost:8080`
**Note**: To deploy your static site to a static hosting platform you will have to deploy the `dist/browser` folder, rather than the usual `dist`


## Universal "Gotchas"
Moved to [/angular/universal/docs/gotchas.md](/angular/universal/blob/fabian/readme-logo/docs/gotchas.md)

# License
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](/LICENSE)
