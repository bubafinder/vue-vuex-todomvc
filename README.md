# Cypress + Percy Workshop

## Pre-requisites
### MacOS
1. Install VS Code - https://code.visualstudio.com/download
2. Install Node.JS - https://nodejs.org/en/download
3. Install Git - https://git-scm.com/download/mac

### Windows 
1. Install VS Code - https://code.visualstudio.com/download
2. Install Node.JS - https://nodejs.org/en/download
3. Install Git - https://git-scm.com/download/win
#
## Setup App
1. Clone repository
2. Run `npm install`
3. Run `npm start` - Start App

## Running Cypress
Run `npm run dev` - Start App and Cypress

Run `npm run cy:open` - Open Cypress

## Percy
Username: mlovric+dump@extensionengine.com

Password: ******

export PERCY_TOKEN=web_a7cebe60b9911dcc6be846b785cb2759c407f87550eb77e8d61c45bfe197fa7d



#

# vue-vuex-todomvc [![renovate-app badge][renovate-badge]][renovate-app] [![ci status][ci image]][ci url] ![cypress version](https://img.shields.io/badge/cypress-11.2.0-brightgreen)

Simple TodoMVC with [Vue.js](https://vuejs.org/)
and [Vuex](https://vuex.vuejs.org/en/) data store.

Based on [this Vuex tutorial](https://codeburst.io/build-a-simple-todo-app-with-vue-js-1778ae175514) and the basic official [TodoMVC vue.js example](https://github.com/vuejs/vue/tree/dev/examples/todomvc)

Read my [step by step tutorial](https://glebbahmutov.com/blog/vue-vuex-rest-todomvx/) explaining the code and this [thorough blogpost](https://www.cypress.io/blog/2017/11/28/testing-vue-web-application-with-vuex-data-store-and-rest-backend/) how this application is tested using Cypress.

## Software organization

![Vue Vuex REST data flow](vue-vuex-rest.png)

## Use

Clone this repository then

```
npm install
npm start
```

Open `localhost:3000` in the browser.

## Tests

All tests are implemented using [Cypress.io](https://www.cypress.io/)

- [GUI E2E tests](cypress/integration/ui-spec.js)
- [API tests](cypress/integration/api-spec.js)
- [Vuex store tests](cypress/integration/store-spec.js)

### cy-spok example

See the spec [new-item-spec.js](./cypress/integration/new-item-spec.js) that shows how to use [cy-spok](https://github.com/bahmutov/cy-spok) plugin to confirm the request object. Watch the introduction to cy-spok plugin video [here](https://youtu.be/MLDsqBd_gVU).

## Development

The `app` global variable exposes the Vue instance.

To see "plain" values from the store (without all `Observer` additions)

```js
app.$store.getters.todos
    .map(JSON.stringify) // strips utility fields
    .map(JSON.parse)     // back to plain objects
    .forEach(t => console.log(t)) // prints each object
```

Or print them as a table

```js
console.table(app.$store.getters.todos.map(JSON.stringify).map(JSON.parse))
```

## Small print

Author: Gleb Bahmutov &lt;gleb.bahmutov@gmail.com&gt; &copy; 2021

- [@bahmutov](https://twitter.com/bahmutov)
- [glebbahmutov.com](https://glebbahmutov.com)
- [blog](https://glebbahmutov.com/blog)
- [videos](https://www.youtube.com/glebbahmutov)
- [presentations](https://slides.com/bahmutov)
- [cypress.tips](https://cypress.tips)

License: MIT - do anything with the code, but don't blame me if it does not work.

Support: if you find any problems with this module, email / tweet /
[open issue](https://github.com/bahmutov/vue-vuex-todomvc/issues) on Github

[ci image]: https://github.com/bahmutov/vue-vuex-todomvc/workflows/ci/badge.svg?branch=master
[ci url]: https://github.com/bahmutov/vue-vuex-todomvc/actions
[renovate-badge]: https://img.shields.io/badge/renovate-app-blue.svg
[renovate-app]: https://renovateapp.com/
