# Angular Interview Questions & Answers
--------
| No. | Questions |
|---- | ---------
|1 | [Hoisting?](#hoisting)|
|2 | [Closure?](#closure)|
|3 | [Ngrx?](#ngrx)|


--------
1. ### Hoisting
    Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution

    ```
    function hoist() {
		  a = 20;
		  var b = 100;
		}
		
		hoist();
		console.log(a); 	// it will print a value as 20
		console.log(b); 	// it will make an error as ReferenceError, where b is local to hoist
    ```

2. ### Closure
    A closure is the combination of a function enclosed with references to its surrounding state . In other words, a closure gives you access to an outer function's scope from an inner function

3. ### Ngrx