JavaScript:

    # Declare a variable using let or const.
        let myVariable = 'hello';
        const myConstant = 42;

    # Log a message to the console.
        console.log('Hello, world!');

    # Alert a message to the user.
        alert('Hello, user!');

    # Prompt the user for input.
        let userInput = prompt('What is your name?');

    # Declare a function.
        function myFunction(arg1, arg2) {
            Function body goes here.
        }

    # Call a function.
        myFunction(value1, value2);

    # Declare an object.
        let myObject = {
            key1: 'value1',
            key2: 'value2',
            key3: 'value3',
        };

    # Access an object's property.
        myObject.key1;

    # Declare an array.
        let myArray = [1, 2, 3, 4];

    # Access an array's element.
        myArray[0];

    # Declare a for loop.
        for (let i = 0; i < myArray.length; i++) {
            Loop body goes here.
        }

    # Declare a while loop.
        while (condition) {
            Loop body goes here.
        }

    # Declare an if statement.
        if (condition) {
            Code to execute if condition is true.
        }

    # Declare an if-else statement.
        if (condition) {
            Code to execute if condition is true.
        } else {
            Code to execute if condition is false.
        }

    # Declare a switch statement.
        switch (expression) {
            case value1:
                Code to execute if expression equals value1.
                break;
            case value2:
                Code to execute if expression equals value2.
                break;
            default:
                Code to execute if expression doesn't match any case.
        }

    # Declare a try-catch block.
        try {
            Code that might throw an error.
        } catch (error) {
            Code to handle the error.
        }

    # Declare a timeout function.
        setTimeout(function() {
            Code to execute after a delay.
        }, delay);

    # Declare an interval function.
        setInterval(function() {
            Code to execute repeatedly at an interval.
        }, interval);

    # Declare a callback function.
        function myFunction(callback) {
            Code to execute before the callback.
            callback();
            Code to execute after the callback.
        }

    # Declare a promise.
        let myPromise = new Promise(function(resolve, reject) {
            Code that might resolve or reject the promise.
        });

    # Use the then method of a promise.
        myPromise.then(function(result) {
            Code to execute if the promise resolves successfully.
        }).catch(function(error) {
            Code to execute if the promise is rejected.
        });

    # Declare a class.
        class MyClass {
            constructor(arg1, arg2) {
                Constructor code goes here.
            }
            myMethod(arg1, arg2) {
                Method body goes here.
            }
        }

    # Declare a module.
        export function myFunction(arg1, arg2) {
            Code to export goes here.
        }

    # Import a module
        import { myFunction } from './my-module.js';
