# First Version<!-- omit in toc -->

## Table of Contents<!-- omit in toc -->
- [Install Node.js, NPM and NPX](#install-nodejs-npm-and-npx)
- [Run React Application](#run-react-application)
- [Modifiyng the React App](#modifiyng-the-react-app)
- [Structure the Frontend App](#structure-the-frontend-app)
- [Reinstall all dependencies](#reinstall-all-dependencies)
- [Create Production Build](#create-production-build)
  - [Use the build](#use-the-build)
  - [Test / Run locally](#test--run-locally)
- [Next steps](#next-steps)
- [Clean up Default React App](#clean-up-default-react-app)
- [How is everything working](#how-is-everything-working)
- [React Functional Components](#react-functional-components)

Only frontend, singlepage using Unsplash API

Written in React with
1. Header
2. Input field
3. Search button (with Unsplash API)
4. Image cards

Unsplash API: `https://unsplash.com/`

## Create React App<!-- omit in toc -->

**Create React App [LINK](https://reactjs.org/docs/create-a-new-react-app.html):** Package 

**npx:** Package runner within `npm 5.2+`

We can run a library only once.

**npm (Node.js Package Manager) [LINK](https://www.npmjs.com):** It is used to install npm packages like `create-react-apps`. It is installed around Node.js


**Node.js [LINK](https://nodejs.org/en/):** JavaScript runtime environment, built on Chrome web Browser to run JavaScript apps. 

   - For running React, you dont require Node.js
   - Node.js is required if you run development build of the React app created with `create-react-app`.

### Install Node.js, NPM and NPX

To check for installation, type `node --version` on terminal. If you can see the version, it is installed. The same works with npm and npx `npm --version`.

[LINK](https://nodejs.org/en/)

After installing Node.js, tyoe in terminal (in the folder you want your React app to be in) `nps create-react-app my_app`, to use another version of the create react app library, type `create-react-app@4.0.1`.

### Run React Application

To run the react application, locate in the created folder (in this case `frontend`) in terminal and write the command `npm start`.

It should initiate a browser with localhost open. It uses for default the port 3000.

### Modifiyng the React App

To modify the reat app, simply go to the files inside the created folder.

Files could be modified while the app is running and it will update automatically.

### Structure the Frontend App

We see multiple folders and new files.

1. File `package.json`
   Is usually present in every JS app. It has variables for configuration.
   1. Name
   2. App version
   3. Set of dependencies (dependency and version): Those are installed in our proyect and we will use:
      - react
      - react-dom
      - react-scripts
   4. Scripts: Those scripts are executed under the hood when u enter `npm --script_name--`, buyt an other kinds of command you will have to write `npm run build` for example.
   5. eslintConfig: Section for configuration of the linter
   6. Browsers list: divides in production and development settings.

2. `README.md`: Used for making it easy to know commands and start with React.
3. .gitignore: Used for git to ignore certain files in the repository and not track them.
4. .eslintcashe: Cache for eslint, we will add it to `.gitignore`. In versions 4.0.3 of `create-react-app`, it is not created in root folder, Create it in the folder `frontend`.
5. SCR FOLDER: All application related to the app should be included here
6. PUBLIC FOLDER: Static files for a web browser to run the application.
7. NODE_MODULES FOLDER: Contains all dependencied installed. Dependencies can have their own dependencies, that's why node_modules folder is so big and should not be commited.

### Reinstall all dependencies

If we delete `node_modules` folder, app fails to run, as it doesn't have it's dependencies. `react-scripts: command not found`. 

To install all dependencies, just write `npm install`.

All those modules are located in `node_modules` folder. Here we can find executables for `react-start`or any other script we use.

If you run the app via terminal with `npm start`, it runs `react-scripts start`. 

### Create Production Build

1. Terminate app with `control+c`
2. Locate in Terminal within `frontend`folder (or React project location)
3. run command `npm run build`
4. A folder names `build`must have been created

#### Use the build

Just copy the contents of the folder `build` to a web server.

#### Test / Run locally

To test the build, we can use the npm package `serve`. Serve package can be installed globally with command `npm install -g serve` and then run the build with `serve -s build`.

If you want to use `serve` just once and not install it on your device, you could use `npx serve -s build`.

### Next steps

1. Clean up default React App
2. Initialize Git Repository
3. Replace favicon
4. Install `react-bootstrap`: Includes different React components like the `button` component, and later adjust those components.
5. Create Header, Search, Welcome and ImageCard components
6. Configure ESLint and Prettier to fix and auto format code on filesave
7. Use fetch to search images on Unsplash

### Clean up Default React App

1. Remove everything whithin the App div in `App.js`.
2. Delete line 1 (logo import) (TIP: `command+shift+k`).
3. Delete line 2 (`.App.css`) and space below.
4. Delete file `logo.svg` on src folder.
5. Delete file `App.css` on src folder.
6. Delete file `App.test.js` on src folder.
7. Delete file `reportWebVitals.js` on src folder. Used for reporting user activity on the app.
8. Delete file `setupTests.js` on src folder.
9. Remove lines for importing `reportWebVitals.js` on index/js and to run `reportWebVitals()`.
10. Remove `code` section on `index.css` file.
11. Create folder `css` on src folder to keep all `.css` files (including existing `index.css` file).
12. Adjust location for `index.css` on `index.js`.

### How is everything working

In `index.js` file, there are several imports. The first two lines were installed with all the other dependencies when we typed in terminal `npm install` inside the project folder.

**react-dom:** Stands for Document Object Model and it is  what we see in browser (what it renders).

Inside `index.js` file, we see method `ReactDOM.render()`, and it is called with tqo arguments:
1. [JSX sintax](https://reactjs.org/docs/introducing-jsx.html) is used by React to create its elements. It is translated into normal JavaScript. for web browser interpretation. In this part resides the whole React App. We can also use some normal HTML with no problems.
2. `document.getElementById('root')`: We see a variable called `document`, which is a global variable, defined as an HTML file, located in the folder `public`, and ir has a div with `id=root`.

React components are mentioned with capital letter.

To enter JS syntax inside JSX, just use `{}`.

### React Functional Components

These are defined using functions inside `App.js` file. Arrow or normal.

JSX syntax converts lines of HTML into JS by just using the method `React.createElement()`.