# Task List React AWS

This is a learning project to help brush up on full stack AWS skills.

This project follows the free tutorial instruction on YouTube: https://www.youtube.com/watch?v=FHn8c4Rk_yo

Thank you to the [Code With Vini](https://www.youtube.com/@codewithvini1644) YouTube channel.

Cheers :)

## Create ReactJS App

The following command was used to create the initial ReactJS bootstrap files:

```
cd ui_react
npx create-react-app .
```

After `create-react-app` completes, verify the boilerplate ReactJS app was successfully created:

./ui_react
```
npm start
```

This should show the boilerplate ReactJS app appear in a browser. 

Because this repo should be a `Mono-repo`, remove the git version control folder, `.git` created with this ReactJS app:

./ui_react
```
rm -rf .git
```

The repo will be created at the root of this `Mono-repo` instead of in the individual sub-project folders. 

Install the [Material UI Core](https://mui.com/material-ui/getting-started/installation/) library into the ReactJS project:

./ui_react
```
npm install @mui/material @emotion/react @emotion/styled
```

Also install Material icons:

./ui_react
```
npm install @mui/icons-material
```

Install [axios](https://www.npmjs.com/package/axios) and [classnames](https://www.npmjs.com/package/classnames) node modules:

./ui_react
```
npm install axios classnames
```

Remove files that aren't needed:

./ui_react/src/
```
logo.svg
reportWebVitals.js
setupTests.js
App.test.js
App.css
```

Remove the imports that are no longer in the project, from `./ui_react/src/App.js` and replace the contents of the `<div className="App">` with "Hello World".

Clear out the `./ui_react/src/index.css` file so that it's blank.

Remove `reportWebVitals` from `./ui_react/src/index.js` and remove `<React.StrictMode>`. 

Finally, confirm that the ReactJS app still starts with `npm start`. There should just be a "Hello World" blank page.

Move the `.gitignore` to the root of the project and add `/ui_react` into the .gitignore.

After these steps above, this is the first commit of the project. 

## VSCode Extensions Used in this Tutorial

- [ES7+ React/Redux/React-Native snippets](https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets) by dsznajder

Example usage - create boilerplate code:
```
# React Arrow Function Component
rafc 
```

- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) by Prettier

## Initialize the API Sub Project

Just use the defaults (hit enter) when initializing npm:

./api_express
```
npm init
```

Install all of the dependencies for the API:

./api_express
```
npm install express nodemon cors serverless-http @aws-sdk/client-dynamodb @aws-sdk/lib-dynamodb
```

Delete the `test` under "scripts" in `./api_express/package.json` and replace it with:

```
    "start": "node index",
    "dev": "DEVELOPMENT=true nodemon index"
```

The above "dev" script name sets an environment variable, `DEVELOPMENT` with a value of "true". `nodemon allows hot reload of the app.

Add `"type": "module",` to `./api_express/package.json` so that `imports` can be used instead of `require`. 

