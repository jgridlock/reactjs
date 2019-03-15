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
    * Additiona info:
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
        * 