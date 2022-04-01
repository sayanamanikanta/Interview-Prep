# JavaScript
--------

### Table of Contents

| No. | Questions |
|---- | ----------|
|1 | [What is an JavaScript](#what-is-an-javascript)|
|2 | [Applications of Javascript Programming](#applications-of-javascript-programming)|
|3 | [JavaScript Variables and Constants](#javascript-variables-and-constants)|
|4 | [var Vs let](#var-vs-let)|
|5 | [Data Types](#data-types)|
|6 | [Hoisting](#hoisting)|
|7 | [Getter and Setter](#getter-and-setter)|
|8 | [Arrays](#arrays)|
|9 | [JavaScript String](#javascript-string)|
|10 | [JavaScript Number](#javascript-number)|
|11 | [Spread Operator](#spread-operator)|
|12 | [Set and WeakSet](#set-and-weakset)|
--------

1. ### What is an JavaScript
    JavaScript is a lightweight and most commonly used as a part of web pages, whose implementations allow client-side script to interact with the user and make dynamic pages. It is an interpreted programming language with object-oriented capabilities

    **[⬆ Back to Top](#table-of-contents)**

1. ### Applications of Javascript Programming
    * Client side validation
    * Manipulating HTML Pages
    * User Notifications
    * Back-end Data Loading
    * Presentations 
    * Server Applications

    **[⬆ Back to Top](#table-of-contents)**

1. ### JavaScript Variables and Constants
    In JavaScript, we use either **var** or **let** keyword to declare variables
    ```js
    var x;
    let y;
    ```

    The const keyword was also introduced in the ES6(ES2015) version to create constants. For example
    ```js
    const x = 5;
    ```
    Once a constant is initialized, we cannot change its value. Simply, a constant is a type of variable whose value cannot be changed

    **[⬆ Back to Top](#table-of-contents)**


1. ### var Vs let
    | var | let |
    | --- | --- |
    | var is used in the older versions of JavaScript | let is the new way of declaring variables starting ES6 (ES2015) |
    | var is function scoped | let is block scoped |

    **[⬆ Back to Top](#table-of-contents)**

1. ### Data Types
    There are eight basic data types in JavaScript. They are
    * String
    * Number
    * BigInt
    * Boolean
    * undefined
    * null
    * Symbol
    * Object

    **[⬆ Back to Top](#table-of-contents)**

1. ### Hoisting
    Hoisting in JavaScript is a behavior in which a function or a variable can be used before declaration

    ```js
    console.log(test);
    var test;
    ```

    In terms of variables and constants, keyword var is hoisted and let and const does not allow hoisting.

    **[⬆ Back to Top](#table-of-contents)**

1. ### Getter and Setter
    In JavaScript, there are two kinds of object properties
    * **Data properties:**
        ```js
        const student = {
            // data property
            firstName: 'Monica';
        };
        ```
    * **Accessor properties:** accessor properties are methods that get or set the value of an object. For that, we use these two keywords
        * **get** - to define a getter method to get the property value
        * **set** - to define a setter method to set the property value
        ```js
        const student = {
            // data property
            firstName: '',

            //accessor property(setter)
            set changeName(newName) {
                this.firstName = newName;
            }

            // accessor property(getter)
            get getName() {
                return this.firstName;
            }    
        }

        // change(set) object property using a setter
        student.changeName = 'Sarah';

        // accessing getter methods
        console.log(student.getName);   // Sarah

        ```

    **[⬆ Back to Top](#table-of-contents)**

1. ### Arrays
    An array is an object that can store multiple values at once

    **Array Methods**
    * **concat()** - joins two or more arrays and returns a result
    * **indexOf()** - searches an element of an array and returns its position
    * **find()** - returns the first value of an array element that passes a test
    * **findIndex()** - returns the first index of an array element that passes a test
    * **forEach()** - calls a function for each element
    * **includes()** - checks if an array contains a specified element
    * **push()** - aads a new element to the end of an array and returns the new length of an array
    * **unshift()** - adds a new element to the beginning of an array and returns the new length of an array
    * **pop()** - removes the last element of an array and returns the removed element
    * **shift()** - removes the first element of an array and returns the removed element
    * **sort()** - sorts the elements alphabetically in strings and in ascending order
    * **slice()** - selects the part of an array and returns the new array
    * **splice()** - removes or replaces existing elements and/or adds new elements

    **Multidimensional Array**
    A multidimensional array is an array that contains another array
    ```js
    const data = [[1, 2, 3], [1, 3, 4], [4, 5, 6]];
    ```

    **[⬆ Back to Top](#table-of-contents)**

1. ### JavaScript String
    JavaScript string is a primitive data type that is used to work with texts

    **String Methods**
    * **charAt(index)** - returns the character at the specified index
    * **concat()** - joins two or more strings
    * **replace()** - replaces a string with another string
    * **split()** - converts the string to an array of strings
    * **substr(start, length)** - returns a part of a string
    * **substring(start,end)** - returns a part of a string
    * **slice(start, end)** - returns a part of a string
    * **toLowerCase()** - returns the passed string in lower case
    * **toUpperCase()** - returns the passed string in upper case
    * **trim()** - removes whitespace from the strings
    * **includes()** - searches for a string and returns a boolean value
    * **search()** - searches for a string and returns a position of a match

    **[⬆ Back to Top](#table-of-contents)**

1. ### JavaScript Number
    numbers are primitive data types in JavaScript

    **Number Methods**
    * **isNaN()** - determines whether the passed value is NaN
    * **isFinite()** - determines whether the passed value is a finite number
    * **isInteger()** - determines whether the passed value is an integer
    * **isSafeInteger()** - determines whether the passed value is a safe integer
    * **parseFloat(string)** - converts the numeric floating string to floating-point number
    * **parseInt(string, [radix])** - converts the numeric string to integer
    * **toExponential(fractionDigits)** - returns a string value for a number in exponential notation
    * **toFixed(digits)** - returns a string value for a number in fixed-point notation
    * **toPrecision()** - returns a string value for a number to a specified precision
    * **toString([radix])** - returns a string value in a specified radix(base)
    * **valueof()** - returns the numbers value
    * **toLocaleString()** - returns a string with a language sensitive representation of a number

    **[⬆ Back to Top](#table-of-contents)**

1. ### Spread Operator
    The spread operator **...** is used to expand or spread an iterable or an array. For example
    ```js
    const arrValue = ['My', 'name', 'is', 'Jack'];

    console.log(arrValue);   // ["My", "name", "is", "Jack"]
    console.log(...arrValue); // My name is Jack
    ```

    **Copy Array Using Spread Operator**
    ```js
    const arr1 = ['one', 'two'];
    const arr2 = [...arr1, 'three', 'four', 'five'];

    console.log(arr2); // ["one", "two", "three", "four", "five"]
    ```


    **[⬆ Back to Top](#table-of-contents)**

1. ### Set and WeakSet
    Set is similar to an array that allows us to store multiple items like numbers, strings, objects, etc. However, unlike an array, a set cannot contain duplicate values
    ```js
    const set3 = new Set([1, 1, 2, 2]);

    console.log(set3); // Set {1, 2}
    ```

    **WeakSet**
    The WeakSet is similar to a Set. However, WeakSet can only contain objects whereas a Set can contain any data types such as strings, numbers, objects, etc

    WeakSets have methods **add()**, **delete()**, and **has()**

    **[⬆ Back to Top](#table-of-contents)**

1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions