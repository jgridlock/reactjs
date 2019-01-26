# reactjs

## Dev Environment
* create-react-app
    * Download and install node.js, should come with npm installer.
    * Verify installation by opening a command window.
        * run node --version and npm --version
    * Install create-react-app
        `npm install -g create-react-app`
    * Create a new react app where my-app is the folder name.
        `create-react-app my-app`
    * Start the app by changing directories into my-app.
        `npm start`
    * Addition information for react with vscode
        https://code.visualstudio.com/docs/nodejs/reactjs-tutorial

## Getting Started
* First thing that needs to be edited is
    `my-app\src\App.js`
* Default content:
    ```
    <div className="App">
        <header className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <p>
            Edit <code>src/App.js</code> and save to reload.
          </p>
          <a
            className="App-link"
            href="https://reactjs.org"
            target="_blank"
            rel="noopener noreferrer"
          >
            Learn React
          </a>
        </header>
    </div>
    ```
## Architecture Overview
1. Props + State (Model)
    * These are considered inputs and the difference between them is that state can change. 
2. Render
3. DOM (Document Object Model)
    * This is the direct result of rendering the Model.
4. Events
    * Outputs from DOM that update State

## Components
* Components are the fundamental units of a react application. Each component corresponds to an element in the DOM. The component is responsible for rendering the content of the element and for handling any events that occur within it. Components can be nested (composing components). Outer components are said to own the inner components.
