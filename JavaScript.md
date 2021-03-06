# JavaScript

* Keywords - Words that are built into the JavaScript language, so the computer will recognize them and treats them specically
* Object - Collection of data and actions that we can use in our code.
* console - Keyword that refers to an object.
    * One action, or method, that is built into the console object is the .log() method. 
        * ie. `console.log(10);`
* comment - Notes within code.
    * Single line - //
    * Multi line - /* */
* Data types - Classifications we give data.
    * Number - 2, 33.2, etc..
    * String - ''
    * Boolean - true or false
    * Null - null
    * Undefined - undefined (It also represents the absence of a value though it has a different use than null.)
    * Symbol
    * Object
        * Built in Objects: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects
    * Operators - +, -, *, /, %, +=, -=, *=, /=, ++, --,
    * Concatenation - Combining two strings with +
    * Dot Operator - .toUpperCase(), .startsWith('H'), .trim() (Removes Whitespace), etc..
        * ie. `'Hello'.length = 5`
        * Additional Dot Operators: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/prototype
        * ie. `Math.floor(Math.random() * 50);`
            * Math.random generates a random number between 0 and 1 but we multiply it by 50 so it generates a random number betweeon 0 and 50. Then math.floor rounds the number down to the nearest whole number.
* Variables
    * var - Keyword that creates, or declares, a new variable. Must use camel casing.
        * ie. `var myName = 'Nick';`
    * let - Keyword that can be reassigned.
    * const - Keyword that can not be reassigned and must be assigned a value when declared.
    * template literals:
        ```
        let myPet = 'cat'
        console.log(`I own a pet ${myPet}.`)
        ```
    * typeof - Shows the type of data.
        ```
        let unknown = 'hello';
        console.log(typeof unknown);
        // Output: String
        ```
* Conditions
    * If
        ```
        if (true) {
        console.log('This message will print!'); 
        } else if {
            console.log('Else if, this one!');
        } else {
            console.log('Else, this one!`);
        }
        ```
    * Switch
    ```
    switch(moonPhase){
        case 'full':
            console.log('Howwwwlll!!');
            break;
        case 'mostly full':
            console.log('Arms and legs are getting hairier');
            break;
        case 'mostly new':
            console.log('Back on two feet');
            break;
        default:
            console.log('Invalid item');
            break;
    ```
    * Operators - === or !==, &&, ||, !
    * Short circuit evaluation
        If tool is false then writingUtensil = 'pen'
        `let writingUtensil = tool || 'pen';`
    * Ternary Operator
        ```
        let isNightTime = false;
        isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');
        // Output: Turn off the lights!
        ```
        ```
        let favoritePhrase = 'Love That!';
        favoritePhrase === 'Love That!' ? console.log('I love that!') : console.log("I don't love that!");
        // Output: I love that!
        ```
* Functions
    * Basic function
        ```
        function getReminder(){
            console.log('Water the plants.');
        }
        ```
    * Set default parameters
        ```
        function greeting (name = 'stranger') {
            console.log(`Hello, ${name}!`)
        }
        ```
    * If there is no return statement the value is undefined.
    * Function expressions
        ```
        const plantNeedsWater=function(day,plantNeedsWater){
            if (day === 'Wednesday'){
                return true
            } else {
                return false
            }
        }

        plantNeedsWater('Tuesday'); // Output: false
        ```
    * Arrow function
        ```
        const thisExample = (insert) => {
            return 'one paramter'
        }
        ```
        * No parameters need parentheses
        * One parameter doesnt need parentheses
        * Two or more needs parentheses
* Scope
    * Global variables are anything outside of functions and can be accessed from anywhere.
    * Variable's scope stays within code block `{}`.
* Arrays
    * These are equivalent to python lists `let test = ['cat', 1, true];`
    * If you want to append to an array you can use .push()
    * You can remove the last element of an array with .pop()
    * NOTE: mutatable functions like .push() can be used to change an array within a function and that change will take place outside of the function as well.
* Loops
    * For
        ```
        for (let counter = 0; counter < 4; counter++) {
            console.log(counter);
        }
        ```
        ```
        for (let i = 0; i < vacationSpots.length; i++) {
            console.log('I would love to visit ' + vacationSpots[i]);
        }
        ```
    * While
        ```
        let counterTwo = 1;
        while (counterTwo < 4) {
            console.log(counterTwo);
            counterTwo++;
        }
        ```
        ```
        let countString = '';
        let i = 0;

        do {
            countString = countString + i;
            i++;
        } while (i < 5);
        ```
        * Use break when you want to exit the while loop before the condition is met.
* Higher order functions
    * In a nut shell you can have functions take in functions as a parameter:
        ```
        const checkConsistentOutput = (func, val) => {
        ```
* Iterators
    * .forEach() - loops through every index (sort of like a for i in x)
    * .map() - The map() method creates a new array with the results of calling a function for every array element.
    The map() method calls the provided function once for each element in an array, in order.
        ```
        const bigNumbers = [100, 200, 300, 400, 500];
        const smallNumbers = bigNumbers.map(num => num/100);

        output: [1, 2, 3, 4, 5]
        ```
    * .filter() - The filter() method creates an array filled with all array elements that pass a test (provided as a function).
        ```
        const words = ['chair', 'music', 'pillow', 'brick', 'pen', 'door']; 

        const shortWords = words.filter(word => {
            return word.length < 6;
        });

        output: ['chair', 'music', 'brick', 'pen', 'door']
        ````
    * .findIndex() - returns index of variable that evaluates to true.
    * Additional info:
        * .forEach() is used to execute the same code on every element in an array but does not change the array and returns undefined.
        * .map() executes the same code on every element in an array and returns a new array with the updated elements.
        * .filter() checks every element in an array to see if it meets certain criteria and returns a new array with the elements that return truthy for the criteria.
        * .findIndex() returns the index of the first element of an array which satisfies a condition in the callback function. It returns -1 if none of the elements in the array satisfies the condition.
        * .reduce() iterates through an array and takes the values of the elements and returns a single value.
* Object
    * Objects are basically Python dictionaries:
        ```
        let spaceship = {
            'Fuel Type': 'diesel',
            color: 'silver'
        };
        ```
    * Dot notation can be used to access values or bracket notation
        ```
        const thisColor = spaceship.color;
        const fuel = ['Fuel Type'];
        ```
    * Change values
        ```
        spaceship.color = 'red';   
        ```
    * Add values
        ```
        spaceship.newcolor = 'purple';
        ```
    * Delete values
        ```
        delete sapceship.color;
        ```
    * Objects inside of functions
        ```
        let retreatMessage = 'We no longer wish to conquer your planet. It is full of dogs, which we do not care for.';

        // Write your code below
        const alienShip = {
            retreat() {
                console.log(retreatMessage)
            },
            takeOff() {
                console.log('Blast off')
            }
        };

        alienShip.retreat()
        
        alienShip.takeOff()
        ```
* Advanced objects
    * Use `this` to access objects values within an object:
        ```
        const robot = {
            model: '1E78V2',
            energyLevel: 100,
            provideInfo() {
                return `I am ${this.model} and my current energy level is ${this.energyLevel}`
            }
        };
        ```
    * Getter method - get values inside of objects
        ```
        const robot = {
        _model: '1E78V2',
        _energyLevel: 100,
        get energyLevel() {
            if (typeof this._energyLevel === 'number'){
            return `My current energy level is ${this._energyLevel}`
            } else {
            return 'System malfunction: cannot retrieve energy level'
            }
        }
        };

        console.log(robot.energyLevel)
        ```
    * Setter method - set values inside of objects
        ```
        set energyLevel(){
            some code..
        }

        robot.energyLevel = 200
        ```
    * Factory functions - functions that create objects based on inputs
        ```
        const robotFactory = (model, mobile) => {
            return {
                model: model,
                mobile: mobile,
                beep() {
                console.log('Beep Boop')
                }
            } 
        }
        ```
    * Destructured assignment - shorthand object assignment
        ```
        const robot = {
        model: '1E78V2',
        energyLevel: 100,
        functionality: {
            beep() {
            console.log('Beep Boop');
            },
            fireLaser() {
            console.log('Pew Pew');
            },
        }
        };

        const { functionality } = robot
        functionality.beep()
        ```
* Classes
    * Constructor is like init. Use `new` to create an instance of a class.
        ```
        class Dog {
            constructor(name) {
                this.name = name;
                this.behavior = 0;
            }
        }
        const halley = new Dog('Halley'); // Create new Dog instance
        console.log(halley.name); // Log the name value saved to halley
        // Output: 'Halley'
        ```
    * Full class example with get and accessing instances.
        ```
        class Surgeon {
            constructor(name, department) {
                this._name = name;
                this._department = department;
                this._remainingVacationDays = 20;
            }
            
            get name() {
                return this._name;
            }
            
            get department() {
                return this._department;
            }
            
            get remainingVacationDays() {
                return this._remainingVacationDays;
            }
            
            takeVacationDays(daysOff) {
                this._remainingVacationDays -= daysOff;
            }
            }

            const surgeonCurry = new Surgeon('Curry', 'Cardiovascular');
            const surgeonDurant = new Surgeon('Durant', 'Orthopedics');

            console.log(surgeonCurry.takeVacationDays(3))
            console.log(surgeonCurry.remainingVacationDays)
        ```
    * `super` inherits a variable from the parent class. `new` creates a new instance. Use `extends` to create a child class.
        ```
        class HospitalEmployee {
            constructor(name) {
                this._name = name;
                this._remainingVacationDays = 20;
            }
            
            get name() {
                return this._name;
            }
            
            get remainingVacationDays() {
                return this._remainingVacationDays;
            }
            
            takeVacationDays(daysOff) {
                this._remainingVacationDays -= daysOff;
            }
        }

        class Nurse extends HospitalEmployee {
            constructor(name, certifications){
                super(name);
                this._certifications = certifications;
                this._remainingVacationDays = 20;
            }
        }

        const nurseOlynyk = new Nurse('Olynyk',['Trauma', 'Pediatrics'])
        ```
    * Static methods can only be accessed by calling the Class.method. They can not be accessed from an instance. This example would be within a class.
        ```
            static generatePassword(){
            const randomNumber = Math.floor(Math.random()*10000);
            return randomNumber
        }
        ```
    * Some notes
        * Constructors are created for variables that are going to be accessed in sub classes.
        * Anything with a `this.` in front of it is a property.
        * Getters all you to access properties outside of the class.
        * Setters allow you to change those properties from outside of a class.
        * Methods are used to call getters and setters.
* Modules
    * ES5
        * The pattern we use to export modules is thus:
            Define an object to represent the module.
            Add data or behavior to the module.
            Export the module.
        * Example:
            ```
            let Airplane = {};
            Airplane.myAirplane = 'StarJet';
            module.exports = Airplane;
            ```
        * Import a module with require:
            ```
            const Menu = require('./menu.js');
            ```
    * ES6
        * Exporting modules:
            ```
            export default moduleName;
            ```
        * Importing modules:
            ```
            import Airplane from './airplane';
            ```
        * Exporting specific functions or variables:
            ```
            export { specialty, isVegetarian };
            ```
        * Importing specific functions or variables:
            ```
            import { availableAirplanes, flightRequirements, meetsStaffRequirements } from './airplane';
            ```
        * Importing as:
            ```
            import * as Carte from './menu';

            Carte.chefsSpecial;
            Carte.isVeg();
            Carte.isLowSodium();
            ```
            ```
            import { chefsSpecial as isVeg } from './menu';
            ```
* Promises - Allow for async operation.
    * States:
        ```
        Pending: The initial state— the operation has not completed yet.
        Fulfilled: The operation has completed successfully and the promise now has a resolved value. For example, a request’s promise might resolve with a JSON object as its value.
        Rejected: The operation has failed and the promise has a reason for the failure. This reason is usually an Error of some kind.
        ```
    * Function example, use resolve or reject for pass or fail:
        ```
        function myExecutor(resolve, reject){
            if (inventory.sunglasses > 0){
                resolve('Sunglasses order processed.')
            } else {
                reject('That item is sold out.')
            }
        }
        ```
    * We can expand on this with then statements:
        ```
        prom.then(handleSuccess, handleFailure);
        ```
* Promises in ES8.
    * example:
        ```
        async function withAsync(num){
        if (num === 0){
            return 'zero';
            } else {
            return 'not zero';
            }
        }

        withAsync(100)
        .then((resolveValue) => {
        console.log(` withAsync(100) returned a promise which resolved to: ${resolveValue}.`);
        })
        ```
* Requests
    * example:
        ```
        const xhr = new XMLHttpRequest();
        const url = "https://api-to-call.com/endpoint";
        xhr.responseType = 'json';
        xhr.onreadystatechange = () => {
        if (xhr.readyState === XMLHttpRequest.DONE){
            return xhr.response;
        }
        }

        xhr.open('GET', url);
        xhr.send();
        ```
    * GET request with fetch:
        ```
        fetch('https://api-to-call.com/endpoint').then(response => {
        if (response.ok) {
            return response.json();
        }
        throw new Error('Request failed!');
        }, networkError => {
        console.log(networkError.message);
        }).then(jsonResponse => {
        return jsonResponse;
        });
        ```
# JSX/ReactJS

* JSX
    * Basic units are called elements. JSX is HTML inside of a JS file.
    * JSX elements can be saved just like JS variables:
        ```
        const navBar = <nav>I am a nav bar</nav>;

        const myTeam = {
            center: <li>Benzo Walli</li>,
            powerForward: <li>Rasha Loa</li>,
            smallForward: <li>Tayshaun Dasmoto</li>,
            shootingGuard: <li>Colmar Cumberbatch</li>,
            pointGuard: <li>Femi Billon</li>
        };
        ```
    * JSX elements can have attributes just like HTML.
        ```
        const p1 = <p id="large">foo</p>
        const p2 = <p id="small">bar</p>
        ```
    * You can nest JSX elements just like in HTML. If it is multi line it should look like:
        ```
         const theExample = (
            <a href="https://www.example.com">
                <h1>
                Click me!
                </h1>
            </a>
        );
        ```
    * NOTE: The first opening tag and the final closing tag of a JSX expression must belong to the same JSX element! This can be fixed by wrapping the expression in a <div>
    * Rendering - ReactDOM is a library that contains many specific methods. The first argument should be a JSX expression or a variable that evaluates to a JSX expression. The second element is where that JSX expression is going to get appended to.
        ```
        import React from 'react';
        import ReactDOM from 'react-dom';

        // This is just an example, switch to app.js for the exercise.
        ReactDOM.render(<h1>Hello world</h1>, document.getElementById('app'));
        ```
    * NOTE: React will not update if there is no change in the variable.
    * NOTE: HTML `class` attribute has to be `className` because `class` is reserved in JS.
    * NOTE: HTML self closing tags needs a `/` so `<br>` should be `<br />`.
    * If you add something between `{}` it will execute as JavaScript so this will show 5 on the screen not `2 + 3`:
        ```
        ReactDOM.render(
        <h1>{2 + 3}</h1>,
        document.getElementById('app')
        );
        ```
    * Object properties can be used as elements:
        ```
        const pics = {
            panda: "http://bit.ly/1Tqltv5",
            owl: "http://bit.ly/1XGtkM3",
            owlCat: "http://bit.ly/1Upbczi"
        }; 

        const panda = (
            <img 
                src={pics.panda} 
                alt="Lazy Panda" />
        );
        ```
    * Event listener: https://reactjs.org/docs/events.html#supported-events
        * Even listeners should start with the word on then end in the event `onClick`
    * Conditionals
        * Do the conditionals outside of the JSX:
            ```
            if (coinToss() === 'heads') {
                img = (
                    <img src={pics.kitty} />
                );
            } else {
                img = ( 
                    <img src={pics.doggy} />
                );
            }
            ```
        * Ternary Operator - `x ? y : z` if x is true execute y else do z
            ```
            const headline = (
            <h1>
                { age >= drinkingAge ? 'Buy Drink' : 'Do Teen Stuff' }
            </h1>
            );
            ```
            * NOTE: && can be used to happen or not happen at all
        * Map - use .map() instead of arrays for JSX:
            ```
            const strings = ['Home', 'Shop', 'About Me'];

            const listItems = strings.map(string => <li>{string}</li>);

            <ul>{listItems}</ul>

            // This is fine in JSX, not in an explicit array:

            <ul>
            <li>item 1</li>
            <li>item 2</li>
            <li>item 3</li>
            </ul>

            // This is also fine!

            const liArray = [
            <li>item 1</li>, 
            <li>item 2<li>, 
            <li>item 3</li>
            ];

            <ul>{liArray}</ul>
            ```
        * Key
            * Lists need keys to stay ordered:
                ```
                <ul>
                    <li key="li-01">Example1</li>
                    <li key="li-02">Example2</li>
                    <li key="li-03">Example3</li>
                </ul>
                
                or

                const peopleLis = people.map((person, i) =>
                // expression goes here:
                <li key={'person_' + i}>{person}</li>
                );
                ```
        * NOTE: You can write JSX code in react like so:
            ```
            const h1 = React.createElement(
                "h1",
                null,
                "Hello, world"
            );
            ```
        * Component Instance:
            ```
            import React from 'react';
            import ReactDOM from 'react-dom';

            class MyComponentClass extends React.Component {
            render() {
                return <h1>Hello world</h1>
            }
            }

            ReactDOM.render(
            <MyComponentClass />,document.getElementById('app');
            );
            ```
        * Multiline JSX in a component
            ```
            import React from 'react';
            import ReactDOM from 'react-dom';

            class QuoteMaker extends React.Component {
            render() {
                return (
                <blockquote>
                    <p>
                    The world is full of objects, more or less interesting; I do not wish to add any more.
                    </p>
                    <cite>
                    <a target="_blank"
                        href="https://en.wikipedia.org/wiki/Douglas_Huebler">
                        Douglas Huebler
                    </a>
                    </cite>
                </blockquote>
                );
            }
            };

            ReactDOM.render(
            <QuoteMaker />,
            document.getElementById('app')
            );
            ```
        * Using JS variables
            ```
            const owl = {
            title: 'Excellent Owl',
            src: 'https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-owl.jpg'
            };

            // Component class starts here:
            class Owl extends React.Component {
            render(){
                return (
                <div>
                    <h1>{owl.title}</h1>
                    <img src={owl.src} alt={owl.title}/>
                </div>
                )
            }
            }

            ReactDOM.render(
                <Owl />,document.getElementById('app')
            )
            ```
        * Rendering a variable must be within the render function
            ```
            class Friend extends React.Component{
            render() {
                const friend = friends[2] //this is inside of render function
                return (
                    <div>
                    <h1>
                        {friend.title}
                    </h1>
                    <img src={friend.src} />
                </div>
                )
            }
            }
            ```
        * Conditionals within render
            ```
            class TonightsPlan extends React.Component{
                render(){
                    if(fiftyFifty){
                            return <h1>Tonight I'm going out WOOO</h1>
                    } else {
                    return <h1>Tonight I'm going to bed WOOO</h1>
                    }
                }
                }
            ```
        * Using this. inside of a render
            ```
            class MyName extends React.Component {
                // name property goes here:
                get name(){
                return 'Jonny Smokes'
            }

            render() {
                return <h1>My name is {this.name}.</h1>;
            }
            }
            ```
        * Event listener
            ```
            class Button extends React.Component {
                scream() {
                    alert('AAAAAAAAHHH!!!!!');
                }

                render() {
                    return <button onClick={this.scream}>Scare Me</button>;
                }
                }
            ```
        * Login page example:
            ```
            import React from 'react';
            import ReactDOM from 'react-dom';

            class Contact extends React.Component {
            constructor(props) {
                super(props);
                this.state = {
                password: 'swordfish',
                authorized: false
                };
                this.authorize = this.authorize.bind(this);
            }

            authorize(e) {
                const password = e.target.querySelector(
                'input[type="password"]').value;
                const auth = password == this.state.password;
                this.setState({
                authorized: auth
                });
            }

            render() {
                if(this.state.authorized === true){
                return (
                    <div id="authorization">
                    <h1>Contact</h1>
                    <ul>
                        <li>
                        client@example.com
                        </li>
                        <li>
                        555.555.5555
                        </li>
                    </ul>
                    </div>
                );
                } else {
                const login = (
                    <form action="#" onSubmit={this.authorize}>
                                    <input
                                type="password"
                                placeholder="Password" />
                            <input type="submit" />
                    </form>
                );
                
                const contactInfo = (
                                <ul>
                        <li>
                        client@example.com
                        </li>
                        <li>
                        555.555.5555
                        </li>
                    </ul>
                );
                
                return (
                    <div id="authorization">
                    <h1>Enter the Password</h1>
                        { this.state.authorized ? contactInfo : login }
                    </div>
                );
                }
            }
            }

            ReactDOM.render(
            <Contact />, 
            document.getElementById('app')
            );
            ```
        * Import/export/instantiate
            ```
            export class NavBar extends React.Component{ //export NavBar from js file

            }
            import { NavBar } from './NavBar'; //import NavBar to js file
            <NavBar /> //Call navbar in script
            ```
        * Props - Information can get passed into components and saved as props.
            ```
            <Greeting name="Frarthur" town="Flundon" age={2} haunted={false} />
            ```
            * To access those props you can render them with.
                ```
                this.props.whateverMyPropIs
                ```
            * Event handlers are methods. In this case talk is in the same file but if you wanted to access it from another file you would have to do a `this.props.talk`.
                ```
                class Talker extends React.Component {
                    talk() {
                        let speech = '';
                        for (let i = 0; i < 10000; i++) {
                        speech += 'blah ';
                        }
                        alert(speech);
                    }
                    
                    render() {
                        return <Button talk={this.talk}/>;
                    }
                    }
                ```
            * If a prop is expecting a variable but doesn't recieve anything you can create a default prop:
                ```
                class Button extends React.Component {
                    render() {
                        return (
                        <button>
                            {this.props.text}
                        </button>
                        );
                    }
                    }

                    // defaultProps goes here:
                    Button.defaultProps = { text: 'I am a button' };

                    ReactDOM.render(
                    <Button text=""/>, 
                    document.getElementById('app')
                    );
                ```
            * States are always equal to objects and they setup default properties for classes
                ```
                class App extends React.Component {
                    // constructor method begins here:
                    constructor(props){
                    super(props);
                    this.state = {
                    title: 'Best App'
                    }
                }
                    
                render() {
                    return (
                    <h1>
                        {this.state.title}
                    </h1>
                    );
                }
                }
                ```
            * Whenever you define an event handler that uses this, you need to add this.methodName = this.methodName.bind(this) to your constructor function.
                ```
                class Mood extends React.Component {
                    constructor(props) {
                        super(props);
                        this.state = { mood: 'good' };
                        this.toggleMood = this.toggleMood.bind(this);
                    }

                    toggleMood() {
                        const newMood = this.state.mood == 'good' ? 'bad' : 'good';
                        this.setState({ mood: newMood });
                    }

                    render() {
                        return (
                        <div>
                            <h1>I'm feeling {this.state.mood}!</h1>
                            <button onClick={this.toggleMood}>
                            Click Me
                            </button>
                        </div>
                        );
                    }
                    }
                ```
            * IMPORT: Any time that you call this.setState(), this.setState() AUTOMATICALLY calls .render() as soon as the state has changed.
            * bind - If you use `this` within an event handler you need to bind this in the constructor.
                ```
                class Random extends React.Component {
                    constructor(props){
                        super(props);
                        this.state = { color: [0, 200, 255] }
                        this.handleClick = this.handleClick.bind(this); //THIS
                    }
                    
                    handleClick() {
                        this.setState({ //THIS
                        color: this.chooseColor()
                        })
                    }
                ```