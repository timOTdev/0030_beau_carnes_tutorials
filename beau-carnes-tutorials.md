#JavaScript Basics (complete course)
[View full playlist here](https://www.youtube.com/playlist?list=PLWKjhJtqVAbk2qRZtWSzCIN38JC_NdhW5)

## 1. Variables ✔️
### Variables are containers for storing data values. This video also covers naming conventions.
12/23/2017

## 2. Data Types ✔️️
### The seven data types in JavaScript are boolean, null, undefined, number, string, symbol, and object.
12/23/2017

```js
// JS Nuggets: Data Types

// There are 7 data types

// Boolean. true and false

var data = true;

if (data) {
  console.log("Booleans rule!")
} else {
  console.log("Booleans are lame.")
}

// null. is an assignment value that means “no value”

var n = null;
console.log(n * 32);

// undefined. means a variable has not been declared, or has been declared but has not yet been assigned a value

var a;
console.log(a + 2);

// Number. 42 or 3.14159.

var num = 3.6;
var ber = 6.4;
console.log(num + ber);

// String. "Hey!"

var name = "Beau";
console.log("Hi! My name is " + name);

// Symbol (new in ECMAScript 2015). A data type whose instances are unique and immutable.

var sym1 = Symbol("foo");
var sym2 = Symbol("foo");
console.log(sym1 === sym2)
console.log(String(sym1) === String(sym2))

// Object - An object is a collection of properties, and a property is an association between a name (or key) and a value.

var myCar = new Object();
myCar.make = "Ford";
myCar.model = "Mustang";

console.log(myCar.make);
```

## 3. Numbers ✔️️
### Working with numbers including adding, subtracting, multiplying, dividing, modulus, increment, decrement, and compound assignment.
12/23/2017

## 4. String Basics ✔️️ 
### Strings are a group of characters.
12/23/2017

```js
var myName = 'Beau';

var sentence = "He said \"Hi!\""; // He said Hi!
var sentence = 'He said "Hi!"'; // He said Hi!

/*
Code	Output
\'	single quote
\"	double quote
\\	backslash
\n	newline
\r	carriage return
\t	tab
\b	backspace
\f	form feed
*/

var fullName = 'Beau ' + 'Carnes';  // 'Beau Carnes'

var sentence2 = 'My name is ' + fullName; // 'My name is Beau Carnes'

fullName += ' is my name.'; // 'Beau Carnes is my name'
```

## 5. Strings: bracket notation ✔️️
### Bracket notation allows you to access a specific character in a string.
12/23/2017

## 6. 20 String Methods in 7 Minutes
### String methods featured in this video: charAt, charCodeAt, concat, endsWith, fromCharCode, includes, indexOf, lastIndexOf, match, repeat, replace, search, slice, split, startsWith, substr, substring, toLowerCase, toUpperCase, trim.
12/24/2017

- `slice` and `match` returns arrays

```js
/* 20 String Methods */

var stringOne = "freeCodeCamp is the best place to learn"
var stringTwo = "frontend and backend development"

// charAt()
console.log(stringOne.charAt(1))

// charCodeAt()
console.log(stringOne.charCodeAt(1))

// concat()
console.log(stringOne.concat(stringTwo))

// endsWith()
console.log(stringOne.endsWith("to"))

// fromCharCode()
console.log(String.fromCharCode(114))

// includes()
console.log(stringTwo.includes("end"))

// indexOf()
console.log(stringTwo.indexOf("end"))

// lastIndexOf()
console.log(stringTwo.lastIndexOf("end"))

// match()
console.log(stringTwo.match(/end/g))

// repeat()
console.log(stringOne.repeat(3))

// replace()
console.log(stringTwo.replace(/end/g, "END"))

// search()
console.log(stringTwo.search("end"))

// slice()
console.log(stringTwo.slice(2, 4))

// split()
console.log(stringOne.split(" "))

// startsWith()
console.log(stringOne.startsWith("free"))

// substr()
console.log(stringTwo.substr(2, 4))

// substring()
console.log(stringTwo.substring(2, 4))

// toLowerCase()
console.log(stringOne.toLowerCase())

// toUpperCase()
console.log(stringOne.toUpperCase())

// trim()
var stringThree = "     Subscribe now!      ";
console.log(stringThree.trim())
```

## 7. Functions ✔️️
### Functions are one of the fundamental building blocks in JavaScript. This video covers function definitions, names, arguments, parameters, scope, and nesting functions.
12/24/2017

```js
/* Functions */

function square(number) {
  return number * number;
}

console.log(square(4));

var someVar = "Hat";
function myFun() {
  var someVar = "Shoes";
  console.log(someVar);
}

myFun();
console.log(someVar);

console.log(addSquares(1, 3));

function addSquares(a, b) {
  function square(x) {
    return x * x;
  }
  return square(a) + square(b);
}

a = addSquares(2, 3); // returns 13
b = addSquares(3, 4); // returns 25
c = addSquares(4, 5); // returns 41
```

## 8. Hoisting ✔️️
### Hoisting is when variable and function declarations are processed before any code is executed.
12/24/2017

```js
// JS Nuggets
// Hoisting

// console.log(notDeclared); // Uncaught ReferenceError: notDeclared is not defined

console.log(definedLater);
var definedLater;
definedLater = 'I am defined!'
console.log(definedLater)


console.log(definedSimulateneously);
var definedSimulateneously = 'I am defined!'
console.log(definedSimulateneously)


doSomethingElse();
function doSomethingElse(){
  console.log('I did it!');
}


functionVar(); // Uncaught TypeError: functionVar is not a function
var functionVar = function(){
  console.log('I did it!');
}
```

## 9. Comparison Operators & If Else ✔️️
### Comparison operators like >, <, =>, and =<. Also, use if / else statements to execute a block of code if a specified condition is true.
12/24/2017

```js
/** Comparison Operators & If... Else **/

var isFCCGreat = true;

if (isFCCGreat) {
  console.log("Free Code Camp is amazing!");
} else {
  console.log("Free Code Camp is horrible!");
}; 

// Comparison Operators: > < <= >= == !=

var age = 10;

if (age >= 18) {
  console.log("You are an adult!");
} else if (age < 2) {
  console.log("You are a baby!");
} else if (age < 18) {
  console.log("You are a child!");
};

if (age != 18) {console.log("You are NOT eighteen.")};
```

## 10. == vs === ✔️️
### Differences between abstract and strict equality.
12/24/2017

```js
// JS Nuggets: == vs ===

// == abstract equality

// === strict equality

console.log(3 == "3"); // true
console.log(3 === "3"); // false

console.log(true == '1'); // true
console.log(true === '1'); // false

console.log("This is a string." == new String("This is a string.")); // true
console.log("This is a string." === new String("This is a string.")); // false
```

## 11. Null vs Undefined ✔️️
### Differences between null and undefined.
12/26/2017

```js
// JS Nuggets: Null vs Undefined

var test
console.log(test)

test = null

console.log(test)

console.log(typeof null)
console.log(typeof undefined)
console.log(null === undefined)
console.log(null == undefined)
console.log(null === null)
console.log(null == null)
console.log(!null)
console.log(!!null)
console.log(1 + null)
console.log(1 + undefined)
```

## 12. Logical operators && TRICKS with short-circuit evaluation 
### Logical operators are ‘and’ (&&) and ‘or’ (||). These also allow you to do some tricks using short-circuit evaluation.
12/26/2017

```js
// JS Nuggets: Short-circuit Evaluation
if ( 4 > 5 && 5 > 6 ) {
  console.log("hi")
} else {
  console.log("no")
}

var test = true;
var isTrue = function(){
  console.log('Test is true.');
};
var isFalse = function(){
  console.log('Test is false.');
};

if(test){
//  isTrue();
}

( test && isTrue() );


test = false;
if(!test){
  isFalse(); 
}

( test || isFalse());



function theSameOldFoo(name){ 
  name = name || 'Bar' ;
  console.log("My best friend's name is " + name);
}
theSameOldFoo(); 
theSameOldFoo('Beau'); 
```

## 13. Ternary Operator ✔️️
### The ternary operator, or conditional operator, takes three arguments and is basically a shortened way of writing an if-else statement.
12/26/2017

```js
// JS Nuggets: Ternary Operator

// condition ? expr1 : expr2

var age = 15;

if (age >= 18) {
	console.log("You are an adult!");
} else {
	console.log("You are a kid");
};

console.log((age >= 18) ? "You are an adult!" : "You are a kid.");

var stop;

age > 18 ? (
    console.log("OK, you can go."),
    stop = false
) : (
    console.log("Sorry, you are much too young!"),
    stop = true
);

var firstCheck = false,
    secondCheck = false,
    access = firstCheck ? "Access denied" : secondCheck ? "Access denied" : "Access granted";

console.log(access);
```

## 14. Switch Statements ✔️️
### Control the flow of your program with switch statements.
12/26/2017

```js
// JS Nuggets: Switch Statements

let day;
switch (new Date().getDay()) {
    case 0:
    	day = "Sunday";
        break;
    case 1:
    	day = "Monday";
        break;
    case 2:
    	day = "Tuesday";
        break;
    case 3:
    	day = "Wednesday";
        break;
    case 4:
    	day = "Thursday";
        break;
    case 5:
    	day = "Friday";
        break;
    case 6:
    	day = "Saturday";
}
console.log(day)


var Animal = 'chicken';
switch (Animal) {
  case 'Cow':
  case 'Giraffe':
  case 'Dog':
  case 'Pig':
    console.log('This animal will go on Noah\'s Ark.');
    Break;
  case 'Spoon':
    console.log('A spoon is not an animal!');
    break;
  case 'Dinosaur':
  default:
    console.log('This animal will not be on the Ark.');
}
```

## 15. Arrays ✔️️
### Arrays are ways to store more than one value in a single variable. This video also covers nested arrays and the forEach method.
12/26/2017

```js
/* Array Basics */

var sandwich = ["peanut butter", "jelly", "bread"];

var teams = [["Bulls", 23], ["White Sox", 45]];

console.log(sandwich[1]);

sandwich[1] = "bananas";
console.log(sandwich);

console.log(teams[1][0]);
teams[1][0] = "red socks";
console.log(teams);

sandwich.forEach(function(element) {
    console.log(element);
});
```

## 16. Common Array Method
### Learn how to use 10 different array methods: push, pop, concat, join, reverse, shift, unshift, sort, slice, and splice.
1/8/2018

```js
// JS Nuggets: 10 Common Array Methods

var arr = ["a", "b", "c"];

arr.push("d");
console.log(arr);

console.log(arr.pop());
console.log(arr);

var arr2 = ["g", "q"];
console.log(arr.concat(arr2));
console.log(arr2);

console.log(arr.join("!"));

console.log(arr.reverse());
console.log(arr);

console.log(arr.shift());
console.log(arr);

console.log(arr.unshift("p"));
console.log(arr);

console.log(arr.slice(1,3));

arr.push("i");
arr.push("f");
arr.sort(arr);
console.log(arr);

console.log(arr.splice(2, 2, "JS Nuggets"));
console.log(arr);
```

## 17. Copying Arrays (deep and shallow)
### Shallow copy arrays using slice and the spread operator. Deep copy arrays using JSON.stringify.
1/8/2018

```js
/* Copying Arrays */

var original = [true, true, undefined, false, null];

// slice
var copy1 = original.slice(0);


// spread operator
var copy2 = [...original];
console.log(copy1, copy2);


// DEEP copying
var deepArray = [["freeCodeCamp"]];
var shallowCopy = deepArray.slice(0);

shallowCopy[0].push("is great");
console.log(deepArray[0], shallowCopy[0])

var deepCopy = JSON.parse(JSON.stringify(deepArray));

deepCopy[0].push("is great");
console.log(deepArray[0], deepCopy[0])
```

## 18. Random numbers & parseInt️️️️ ✔ ️ ️
### Create random numbers! Also, use parseInt to convert strings to integers.
1/8/2018

```js
/* Random numbers & parseInt */

// console.log(Math.floor(Math.random() * 20));

function randomRange(min, max) {

  return Math.floor(Math.random() * (max - min + 1)) + min;
}

console.log(randomRange(1, 9));


console.log(parseInt("11", 2));
```

## 19. For Loops ✔
### For loops are one of the most common ways to repeat things in JavaScript.
1/10/2018

```js
/* For Loops */

// for ([initialization]; [condition]; [final-expression]) {}

var ourArray = [];
for (var i = 0; i < 5; i++) {
  if (i > 2) break;
  ourArray.push(i);
}
console.log(ourArray);

var arr = [10,9,8,7,6];
for (var i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}

var arr = [
 [1,2], [3,4], [5,6]
];
for (var i=0; i < arr.length; i++) {
 for (var j=0; j < arr[i].length; j++) {
   console.log(arr[i][j]);
 }
}
```

## 20. While / Do While ✔
### While and do… while are ways to loop over code in JavaScript.
1/10/2018

```js
/* While, Do While */

var n = 0;

while (n < 5) {
  n++;
  
  if (n == 3) break;
  console.log("n = " + n);
}

var i = 0;

do {
  i++;
  console.log("i = " + i);
} while (i < 5);

// &turn_off_js=true
```

## 21. For in / For of
### For… in and for… of loops allow you to loop through property names and values in JavaScript.
1/10/2018

```js
/* for... in / for... of */

// usage

// for (variable in object) {
//   statements
// }

// for (variable of object) {
//   statement
// }

let person = {fname:"Beau", lname:"Carnes", arms:2}; 

let arr = [3, 5, 7];
arr.foo = 'hello';

let text = "";
for (let x in person) {
  text += person[x];
  console.log(x);
};
console.log(text);

for (let i in arr) {
  console.log(i);
};

for (let i of arr) {
  console.log(i);
};

```

## 22. Array Iteration: 8 Methods
### Learn eight methods to iterate through an array in JavaScript! Methods include: forEach, map, filter, reduce, sum, every, find, findIndex.
1/10/2018

```js
// JS Nuggets
// Array iteration: 8 methods

// forEach
[1, 2, 3].forEach(function (item, index) {
  console.log(item, index);
});


// map
const three = [1, 2, 3];
const doubled = three.map(function (item) {
  return item * 2;
});
console.log(doubled);


// filter
const ints = [1, 2, 3];
const evens = ints.filter(function (item) {
  return item % 2 === 0;
});
console.log(evens);


// reduce
const sum = [1, 2, 3].reduce(function (result, item) {
  return result + item;
}, 0);
console.log(sum)


// some
const hasNegativeNumbers = [1, 2, 3, -1, 4].some(function (item) {
  return item < 0;
});
console.log(hasNegativeNumbers);


// every
const allPositiveNumbers = [1, 2, -3].every(function (item) {
  return item > 0;
});
console.log(allPositiveNumbers);


// find
const objects = [{ id: 'a' }, { id: 'b' }, { id: 'c' }];
const found = objects.find(function (item) {
  return item.id === 'b';
});
console.log(found);


// find index
const objects2 = [{ id: 'a' }, { id: 'b' }, { id: 'c' }];
const foundIndex = objects2.findIndex(function (item) {
  return item.id === 'b';
});
console.log(foundIndex)
```

## 23. Objects
### Objects are stand-alone entities with properties and types.
1/10/2018

```js
// JS Nuggets: Objects

var myCar = new Object();
myCar.make = "Ford";
myCar.model = "Mustang";
myCar.color;
console.log(myCar.make);
console.log(myCar.color);

myCar["year"] = 1969;
console.log(myCar["model"])

myCar["Do I like?"] = "I hate my car.";
console.log(myCar["Do I like?"]);



function showProps(obj, objName) {
  var result = "";
  for (var i in obj) {
    // obj.hasOwnProperty() is used to filter out properties from the object's prototype chain
    if (obj.hasOwnProperty(i)) {
      result += objName + "." + i + " = " + obj[i] + "\n";
    }
  }
  return result;
}
console.log(showProps(myCar, "myCar"));

// Creation: object initializer
var myHonda = {color: "red", wheels: 4, engine: {cylinders: 4, size: 2.2}};

// Creation: constructor function
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}

var mycar = new Car("Chevy", "Malibu", 1993);
var anothercar = new Car("Mazda", "Miata", 1990);
console.log(mycar.model);
mycar.color = "black";
console.log(mycar.color);

// Creation: Object.create
var Animal = {
  type: "Invertebrates", 
  displayType: function() {  
    console.log(this.type);
  }
}

var animal1 = Object.create(Animal);
animal1.displayType(); 

var fish = Object.create(Animal);
fish.type = "Fishes";
fish.displayType();
```

## 24. Objects, part 2 ✔
### Learn more about objects. This video covers using objects for lookups, removing properties using delete, testing for properties, accessing and modifying nested objects, and creating an array of all object keys.
1/10/2018

```js
// Objects: Part 2

// Using Objects for Lookups
var alpha = {
  1:"Z",
  2:"Y",
  3:"X",
  4:"W"
  // ...
};
console.log(alpha[2]);

  // Remove Object Properties
let dishes = {
  plates: 8,
  cups: 10,
  forks: 28,
  bowls: 13
};
delete dishes.cups;
console.log(dishes);

// Testing Objects for Properties
console.log(dishes.hasOwnProperty('plates'));
console.log(dishes.hasOwnProperty('cups'));

// Accessing and Modifying Nested Objects
var ourStorage = {
  "desk": {
    "drawer": "stapler"
  },
  "cabinet": {
    "top drawer": {
      "folder1": "a file",
      "folder2": "secrets"
    },
    "bottom drawer": "soda"
  }
};
console.log(ourStorage.cabinet["top drawer:].folder2);
console.log(ourStorage.desk.drawer);

ourStorage.cabinet["top drawer"].folder2 = "cake recipe";
console.log(ourStorage.cabinet["top drawer"].folder2);

// Generate an Array of All Object Keys
console.log(Object.keys(ourStorage));
```

## 25. AJAX
### AJAX in allows allows you to update parts of a web page without reloading the entire page.
1/19/2018

```html
<h1>AJAX with JavaScript!</h1>
<p id="demo">Let AJAX change this text</p> 
<button type="button" onclick="loadDoc()">Change Content</button>
```

```js
// AJAX = Asynchronous JavaScript And XML

function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
     document.getElementById("demo").innerHTML = this.responseText;
    }
  };
  xhttp.open("GET", "https://cors-anywhere.herokuapp.com/http://carnes.cc/code/ajax_example.txt", true);
  xhttp.send();
}

/* 
Adding "https://cors-anywhere.herokuapp.com/" prevents the following error:

XMLHttpRequest cannot load http://carnes.cc/code/ajax_example.txt. No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'https://s.codepen.io' is therefore not allowed access.
*/
```

## 26. JSON
### JSON stands for JavaScript Object Notation. It is a syntax for storing and exchanging data.

```js
//JS Nuggets: JSON

// example
var myJSON = {
    "name": {
        "first": "Beau",
        "last": "Carnes"
    },
    "age":33,
    "skills": [ "juggling", "stiltwalking", "coding" ],
    "married": true,
    "superpowers": null
 }

// stringify method
var stringified = JSON.stringify(myJSON);
console.log(stringified);


// parse method
var stringJSON = '{ "name":"Beau", "kids":2,"state":"Michigan"}';
var myParse = JSON.parse(stringJSON);
console.log(myParse);

```

## 27. Closures
### A closure is the combination of a function and the environment where the function is declared.
1/19/2018

```js
// JS Nuggets: Closures

function makeFunc() {
  var name = "JS Nuggets";
  function displayName() {
    console.log(name);
  }
  return displayName;
}

var myFunc = makeFunc();
myFunc();


var counter = (function() {
  var privateCounter = 0;
  function changeBy(val) {
    privateCounter += val;
  }
  return {
    increment: function() {
      changeBy(1);
    },
    decrement: function() {
      changeBy(-1);
    },
    value: function() {
      return privateCounter;
    }
  };   
})();

console.log(counter.value());
counter.increment();
counter.increment();
console.log(counter.value()); 
counter.decrement();
console.log(counter.value());
```


## 28. this
### The keyword ‘this’ refers to the object that “owns” the JavaScript code.
1/19/2018

```js
/* THIS */

console.log(this.document === document);

console.log(this === window);

this.a = 37;
console.log(window.a); 


function f1() {
  'use strict';
  return this;
}
console.log(f1() === window);



function add(c, d) {
  return this.a + this.b + c + d;
}

var o = {a: 1, b: 3};
console.log(add.call(o, 5, 7));
console.log(add.apply(o, [10, 20]));


function f() {
  return this.a;
}

var g = f.bind({a: 'unicycle'});
console.log(g());

var h = g.bind({a: 'cereal'}); // won’t work a second time
console.log(h());

var o = {a: 8, f: f, g: g, h: h};
console.log(o.f(), o.g(), o.h());


var o = {
 traditionalFunc: function () {
   console.log('traditionalFunc this === o?', this === o);
 },
 arrowFunc: () => {
   console.log('arrowFunc this === o?', this === o);
   console.log('arrowFunc this === window?', this === window);
 }
};

o.traditionalFunc();

o.arrowFunc();


var o = {
  prop: 37,
  f: function() {
    return this.prop;
  }
};

console.log(o.f()); // logs 37

var o = {prop: 23};

function independent() {
  return this.prop;
}

o.f = independent;

console.log(o.f());
```

## 29. Promises
### A promise represents the eventual result of an asynchronous operation.
1/20/2018

```js
// JS Nuggets: Promises

// Basic usage
var p = new Promise(function(resolve, reject) {
	
	// Do an async task async task and then...

	if(good_condition) {
		resolve('Success!');
	}
	else {
		reject('Failure!');
	}
});

p.then(function() { 
	/* do something with the result */
}).catch(function() {
	/* error */
})


// Complete example

var promiseCount = 0;

function testPromise() {
  var thisPromiseCount = ++promiseCount;
  console.log(thisPromiseCount + ': Started - Sync code started');

  var p1 = new Promise(function(resolve, reject) {
    console.log(thisPromiseCount + ': Promise started - Async code started');
    // This is only an example to create asynchronism
    window.setTimeout(
      function() {
        resolve(thisPromiseCount);
      }, Math.random() * 2000 + 1000);
  });

  p1.then(function(val) {
    console.log(val + ': Promise fulfilled - Async code terminated');
  }).catch(function(reason) {
    console.log('Handle rejected promise ('+reason+') here.');
  });

  console.log(thisPromiseCount + ': Promise made - Sync code terminated');
}

testPromise();
testPromise();
testPromise();
```

## 30. Desktop Notifications
### The Notifications API lets a web page or app send notifications that are displayed outside the page at the system level. This lets web apps send information to a user even if the application is idle or in the background.
1/20/2018

```js
// JS Nuggets: Notifications API

//Notification.requestPermission();

//new Notification("Subscribe to JS Nuggets!");

function notifyMe() {
  if (!("Notification" in window)) {
    alert("This browser does not support system notifications");
  }
  else if (Notification.permission === "granted") {
    notify();
  }
  else if (Notification.permission !== 'denied') {
    Notification.requestPermission(function (permission) {
      if (permission === "granted") {
        notify();
      }
    });
  }
  
  function notify() {
    var notification = new Notification('TITLE OF NOTIFICATION', {
      icon: 'http://carnes.cc/jsnuggets_avatar.jpg',
      body: "Hey! You are on notice!",
    });

    notification.onclick = function () {
      window.open("http://carnes.cc");      
    };
    setTimeout(notification.close.bind(notification), 7000); 
  }

}
notifyMe();
```

## 31. Immediately Invoked Function Expression
### An Immediately Invoked Function Expression (IIFE) is a JavaScript function that runs as soon as it is defined.
1/20/2018

```js
/* Immediately Invoked Function Expression (IIFE)  */

(function () {
  console.log("My favorite number is 3");
})();

(favNumber = function (num = 3) {
  console.log("My favorite number is " + num);
})();

favNumber(5);


var a = 2;

(function() {
  var a = 3;
  console.log(a);
})();

console.log(a);

let b = 2;

{
  let b = 3;
  console.log(b);
}

console.log(b);
```

## 32. Strict Mode
### “use strict” — Strict mode in JavaScript tightens the rules for certain behaviors. You can execute JavaScript code in strict mode by using the “use strict” directive.
1/20/2018

```js
"use strict";
/* Strict Mode */

function myFunction() {
  "use strict";
	var y = 3.14;  
}

// CONVERTING MISTAKES INTO ERRORS

var x = 3.14;
delete x;   

var obj = {};
Object.defineProperty(obj, "x", {value:0, writable:false});
obj.x = 3.14;

var obj = {get x() {return 0} };
obj.x = 3.14;

delete Object.prototype;

function sum(a, a, c) { 
  'use strict';
  return a + b + c; 
}


// WITH AND EVAL CHANGES

var x = 17;
with (obj) {
  x; // Is this var x or obj.x?
}

eval("var x;")

var x = 17;
var evalX = eval("'use strict'; var x = 42; x;");
console.assert(x === 17);
console.assert(evalX === 42);


// SECURING JAVASCRIPT
```

## 33. Check if a property is in an object
###How do you check if a property is in an object in JavaScript? Learn three ways in this video. Two of the ways are ‘in’ and ‘hasOwnProperty’.
1/21/2018

```js
// JS Nuggets: Check if a property is in an object

var myObject = {
  name: 'JS Nuggets'
};

if (myObject.name) {
  console.log("it is in!")
}

console.log(myObject.hasOwnProperty('name'));
console.log('name' in myObject);

console.log(myObject.hasOwnProperty('valueOf'));
console.log('valueOf' in myObject);
```

## 34. setInterval and setTimeout: timing events
### setTimeout and setInterval are timing events in JavaScript that both allow execution of code at specified time intervals. This quick tutorial shows how to use them.
1/21/2018

```html
<button onclick="clearInterval(intId)">Stop time</button>
```

```js
/* setTimeout and setInterval */

// setTimeout
var timeoutID = setTimeout(bye, 3000);

console.log('hello');

clearTimeout(timeoutID);

function bye() {
  console.log('goodbye');
}


// setInterval

var count = 0
var intId = setInterval(counter, 1000);
 
function counter() {
  console.log(++count);
}
```

## 35. try, catch, finally, throw — error handling in JavaScript
### Error handling in JavaScript uses the keywords: try, catch, finally, and throw.
1/21/2018

```js
/* Try, catch, finally */

try {
  console.log('Start of try runs');
  
  unicycle;

  console.log('End of try runs -- never reached'); 

} catch(err) {

  console.log('Error has occured: ' + err); 

} finally {
  console.log('This is always run'); 
}

console.log('...Then the execution continues');




let json = '{ "age": 30 }';
 
try {
 
  let user = JSON.parse(json); 
  if (!user.name) {
    throw new SyntaxError("Incomplete data: no name");
  }
 
  console.log( user.name );
 
} catch(e) {
  console.log( "JSON Error: " + e ); 
}
```

## 36. Dates
### Work with dates in JavaScript.
1/21/2018

```js
/* Dates */

var d1 = new Date()
console.log(d1.toTimeString())

var d2 = new Date(2017, 1, 3, 42, 43, 23, 23)
console.log(d2.toString())

var d3 = new Date(929397621000)
console.log(d3.toString())

var d4 = new Date("March 25 2017")
console.log(d4.toString())

console.log(d4.getDay())
d4.setYear(2020)
console.log(d4.toString())

var start = new Date();
doSomething();
var end = new Date();

var elapsed = end.getTime() - start.getTime();
console.log(elapsed);

function doSomething() {
    for(var i = 0; i < 1000000000; i++) {

    }
};
```

#ES6 Basics (complete course)
[View full playlist here](https://www.youtube.com/playlist?list=PLWKjhJtqVAbljtmmeS0c-CEl2LdE-eR_F)

## Var vs Const vs Let ️️️️️️️️✔️️
### Three different ways to declare variables.
1/22/2018

```js
// JS Nuggets: Const vs Let vs Var

// const - for values that never change

const Pi = 3.14
// Pi = 1 //error
console.log(Pi);


// let - for block-level variables

for(let i = 0; i < 3; i++) {
  console.log(i);
}
// console.log(i) //error


// var - for variables available to entire function or program

console.log(j)
for(var j = 0; j < 3; j++) {
  console.log(j);
}
console.log(j)
```

## Classes
### Learn about class expressions, class declarations, and inheritance / extending.
1/22/2018

```js
//**JS Nuggets: Classes**

//**class declaration**
class Person {
  constructor(name, year_born) {
    this.name = name;
    this.year_born = year_born;
  }
  
  get age() {
    return this.calcAge();
  }

  calcAge() {
    return new Date().getFullYear() - this.year_born;
  }
  
  what() {
    console.log(this.name + ' is a person.');
  }
  
  static arms() {
    return 2;
  }
}

var me = new Person("Beau", 1983);
console.log(me.name + " was born in " + me.year_born + "!")
me.what();
console.log(me.name + " has " + Person.arms() + " arms!")

class Juggler extends Person {
  what() {
    super.what();
    console.log(this.name + " is a juggler.");
  }
}

var you = new Juggler ("Jay", 1980);
me.what();
you.what();


//**class expressions**
// unnamed
var Person2 = class {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};

// named
var Person3 = class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};
```

## Symbols
### Symbols are a unique immutable data type.
1/22/2018

```js
// JS Nuggets: Symbols

// Creation

let symbol1 = Symbol('symbol2');
let symbol2 = Symbol('symbol2');
console.log(symbol1 === symbol2);
console.log(typeof symbol1);
console.log('symbol: ' + symbol1.toString());


// Use case 1: Symbols as property keys
   const MY_KEY = Symbol();
    let obj = {};
    
    obj[MY_KEY] = 123;
    console.log(obj[MY_KEY]);


// Use case 2: constants representing concepts
const COLOR_RED    = Symbol('Red');
const COLOR_ORANGE = Symbol('Orange');
const COLOR_YELLOW = Symbol('Yellow');
const COLOR_GREEN  = Symbol('Green');
const COLOR_BLUE   = Symbol('Blue');
const COLOR_VIOLET = Symbol('Violet');

function getComplement(color) {
    switch (color) {
        case COLOR_RED:
            return COLOR_GREEN;
        case COLOR_ORANGE:
            return COLOR_BLUE;
        case COLOR_YELLOW:
            return COLOR_VIOLET;
        case COLOR_GREEN:
            return COLOR_RED;
        case COLOR_BLUE:
            return COLOR_ORANGE;
        case COLOR_VIOLET:
            return COLOR_YELLOW;
        default:
            throw new Exception('Unknown color: '+color);
    }
}
```