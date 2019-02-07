# reactjs

### Dev Environment
* Setup
    1. Download and install node.js, should come with npm installer.
    2. Verify installation by running the following in a command window:

        `node --version and npm --version`

    3. Install create-react-app:

        `npm install -g create-react-app`

    4. Create a new react app where my-app is the app name:

        `create-react-app my-app`

    5. Start the app by changing directories into my-app:

        `cd my-app`
        `npm start`

    * Addition information for react with vscode: https://code.visualstudio.com/docs/nodejs/reactjs-tutorial

### Getting Started
* Get bootstrap for css styling support:
    1. Go to https://getbootstrap.com/
    2. Copy the CSS only url and paste into the browser:

        https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css
    3. Save the CSS file into your project src directory.
    4. Open App.js and import:

        `import './bootstrap.min.css';`
    5. To verify, open the web application, open developer tools and look at Styles. Boostrap should be the third style sheet.
* Renaming for consistency:
    1. App.js

        My-App.js
    2. App.test.js -> My-App.test.js
    3. index.js -> Replace all App with My-App(Including the import)
    4. App.js -> Replace all App with My-App (Except the import) -> Remove all return content and replace with `<div>My-App</div>`
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

# Notes

### Architecture Overview
1. Props + State (Model)
    * These are considered inputs and the difference between them is that state can change. 
2. Render
3. DOM (Document Object Model)
    * This is the direct result of rendering the Model.
4. Events
    * Outputs from DOM that update State

### Components
* Components are the fundamental units of a react application. Each component corresponds to an element in the DOM. The component is responsible for rendering the content of the element and for handling any events that occur within it. Components can be nested (composing components). Outer components are said to own the inner components.
* Note: JSX is the markup language that can be utilized within js code.
* Defining a Component
    ```
    function Hello(props){
        return <h1>Hello at {props.now}</h1>;
    }
    ```
* Rendering a Component
    ```
    import ReactDom from 'react-dom';
    import React from 'react';
    
    function Hello(props){
        return <h1>Hello at {props.now}</h1>;
    }    

    ReactDOM.render(<Hello now={new Date().toISOString()} />,
        document.getElementById('root')
    );
    ```
