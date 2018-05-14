# JavaScript Study Guide #

This information was pulled from [Codecademy's](https://www.codecademy.com/learn/introduction-to-javascript) introduction to JavaScript course and is intended as a recap/ summary of some of the basic JavaScript elements for students switching languages or refreshing their memory.
Please do try the [free online course](https://www.codecademy.com/learn/introduction-to-javascript) as it is very helpful, and always refer to the [Mozilla Developer Network](https://developer.mozilla.org/bm/docs/Web/JavaScript) for more information.

## Types and Operators ##

+ Four essential data types in JavaScript include strings, numbers, booleans, and null.
+ Data is printed, or logged, to the console with `console.log()`
+ Four built-in mathematical operators include `+`, `-`, `*`, and `/`.

JavaScript associates certain properties with different data types.
JavaScript has built-in methods for different data types.
Libraries are collections of methods that can be called without an instance.
You can write single-line comments with `//` and multi-line comments between `/*` and `*/`.

## Variables ##

Variables hold reusable data in a program.
JavaScript will throw an error if you try to reassign `const` variables.
You can reassign variables that you create with the `let` keyword.
Unset variables store the primitive data type `undefined`.
Mathematical assignment operators make it easy to calculate a new value and assign it to the same variable.

+ The `+` operator is used to interpolate (combine) multiple strings.

+ In JavaScript ES6, backticks and `${}` are used to interpolate values into a string.

## Control Flow ##

+ `if`/`else` statements make binary decisions and execute different code based on conditions.
+ All conditions are evaluated to be **truthy** or **falsy**.
+ We can add more conditional statements to if/else statements with **else if**.
+ `switch` statements make complicated if/else statements easier to read and achieve the same result.
+ The **ternary operator** (?) and a colon (:) allow us to refactor simple if/else statements.
+ Comparison operators, including `<`, `>`, `<=`, and `>=` can compare two variables or values.
+ After two values are compared, the conditional statement evaluates to *true* or *false*.
+ The logical operator `&&` checks if both sides of a condition are *truthy*.
+ The logical operator `||` checks if either side is *truthy*.
+ The logical operator `!==` checks if the two sides are *not equal*.
+ An exclamation mark (`!`) *switches* the truthiness / falsiness of the value of a variable.
+ One equals symbol (`=`) is used to assign a value to a variable.
+ Three equals symbols (`===`) are used to check if two variables are equal to each other.

*Switch Statement:*

```javascript
var day = 'monday'
switch (day) {
  case 'monday':
    //Statements executed when the
    //day is equal to monday
    console.log('code review')
    break;
  case 'tuesday':
    //Statements executed when the
    //day is equal to tuesday
    console.log('yoga')
    break;
  default:
    //Statements executed when
    //day is equal to anything else
    console.log('write code')
    break;
}
```

## Functions ##

+ Functions are written to perform a task.
+ Functions take data, perform a set of tasks on the data, and then return the result.
+ We can define parameters to be used when calling the function.
+ When calling a function, we can pass in arguments, which will set the function's parameters.
+ We can use `return` to return the result of a function which allows us to call functions anywhere, even inside other functions.

*Regular function syntax:*
```javascript
function plusTwo(num) {
   return num + 2;
 }
```
*Arrow syntax:*
```javascript
var plusTwo = (num) => num + 2
```

## Scope ##

+ *Scope* is the idea in programming that some variables are accessible/inaccessible from other parts of the program.
+ **Global Scope** refers to variables that are accessible to every part of the program.
+ **Block Scope** refers to variables that are accessible only within the block they are defined


## Arrays ##

+ Arrays are lists and are a way to store data in JavaScript.
+ Arrays are created with brackets `[]`.
+ Each item inside of an array is at a numbered position, *starting at 0*.
+ We can **access** one item in an array using its numbered position, with syntax like: `myArray[0]`.
+ We can also **change** an item in an array using its numbered position, with syntax like `myArray[0] = "new string"`;
+ Arrays have a `.length` property, which allows you to see how many items are in an array.
+ Arrays have their own methods, including `.push()` and `.pop()`, which add and remove items from an array, respectively.
+ Arrays have many other methods that perform different functions, such as `.slice()` and `.shift()`. You can read the documentation for any array method on the **Mozilla Developer Network website**.
+ Variables that contain arrays can be declared with `let` or `const`. **Even when declared with const, arrays are still mutable**; they can be changed. However, **a variable declared with const cannot be reassigned.**

## Loops ##

+ `for` loops allow us to repeat a block of code a **known amount of times**.
+ We can use a *for loop inside another for loop to compare two lists*.  
*Basic for loop syntax:*
```javascript
for (i = 0; i < 5; i++) {
    console.log("Let's print the numbers 0 to 4: ${i}");
}
```
+ `while` loops are for looping over a code block an **unknown amount of times**.
+ *Infinite loops occur when stop conditions are never met.*  
*Basic while loop syntax:*
```javascript
var i = 0
while (i < 5) {
    text += "The number is " + i;
    i++;
}
```

## Iterators ##

+ `.forEach()` is used to execute the same code on every element in an array but **does not change the array and returns undefined.**
+ `.map()` executes the same code on every element in an array and **returns a new array with the updated elements.**
+ `.filter()` checks every element in an array to see if it meets certain criteria and **returns a new array with the elements that return truthy for the criteria.**
+ All iterator methods can be written using arrow function syntax. In fact, *given the succinctness and the implicit return of arrow function syntax, this is quickly becoming the preferred way to write these types of method calls.*

+ Additional iterator methods such as `.some()`, `.every()`, `.reduce()` perform different functions.

## Objects ##

+ Objects store **key-value pairs** and let us represent real-world things in JavaScript.
+ **Properties** in objects are **separated by commas**. **Key-value pairs** are always separated by a **colon**.
+ You can **add or edit a property** within an object with **dot notation**.
+ *A method is a function in an object.*
+ `this` helps us with scope inside of object methods. `this` is a dynamic variable that can change depending on the object that is calling the method.
+ **Getter** and **setter** methods allow you to process data before accessing or setting property values.

## Classes ##

+ Classes are templates for objects.
+ Javascript calls a *constructor method* when we create a new instance of a class.
+ Inheritance is when we create a parent class with properties and methods that we can extend to child classes.
+ We use the `extends` keyword to create a subclass.
+ The `super` keyword calls the constructor() of a parent class.
+ **Static methods** are called on the class, but **not on instances of the class**.

## Modules ##

+ Modules in JavaScript are reusable pieces of code that can be exported from one program and imported for use in another program.

+ `module.exports` **exports** the module for use in another program.
+ `require()` **imports** the module for use in the current program.

+ **ES6** introduced a more flexible, easier syntax to export modules:

+ default exports use `export default` to export JavaScript objects, functions, and primitive data types.
+ named exports use the `export` keyword to export data in variables.
+ named exports can be aliased with the `as` keyword.
+ `import` is a keyword that imports any object, function, or data type.
