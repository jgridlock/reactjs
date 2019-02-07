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
        '''
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
    * Operators - === or !===, &&, ||, !
    * Short circuit evaluation
        If tool is false then writingUtensil = 'pen'
        `let writingUtensil = tool || 'pen';`
