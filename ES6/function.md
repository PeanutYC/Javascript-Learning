<ol>
  <li>Write arrow function.</li>
  
```javascript
const myFunc = () {
  const myVar = "value";
  return myVar;
}

//arrow func
const myFunc = () => "value";
```
  <li>Write arrow function with one parameter.</li>
  
```javascript
const doubler = function(item){
  return item * 2;
}
  
//arrow func
const doubler = (item) => item * 2;
doubler(4);

//it's okay to exclude the "()" sign for one parameter
const doubler = item => item *2;
```
  <li>Concat.</li>
  
```javascript
const myConcat = (arr1, arr2) => arr1.concat(arr2);

console.log(myConcat([1, 2], [3, 4, 5]));
```
  
  <li>Rest parameters</li>
  
```javascript
const sum = (...args) => args.reduce((a,b) => a + b, 0);
console.log(sum(1));
```
  
  <li>Spread operators.</li>
  
```javascript
const arr1 = ['JAN', 'FEB', 'MAR', 'APR', 'MAY'];
let arr2;

arr2 = [...arr1];
  
//will not affect arr2
arr1.push("JUN");
console.log(arr2);
```
  
  <li>Use destructuring assignment to extract values from objects</li>
  
```javascript
const HIGH_TEMPERATURES = {
  yesterday: 75,
  today: 77,
  tomorrow: 80
}
  
const { today, tomorrow } = HIGH_TEMPERATURES;
```

   <li>Use destructuring assignment to assign values from objects</li>
  
```javascript
const HIGH_TEMPERATURES = {
  yesterday: 75,
  today: 77,
  tomorrow: 80
};

const {today: highToday, tomorrow: highTomorrow} = HIGH_TEMPERATURES;  
```

   <li>Use destructuring assignment to assign variables from nested objects</li>
  
```javascript
const LOCAL_FORECAST = {
  yesterday: { low: 61, high: 75 },
  today: { low: 64, high: 77 },
  tomorrow: { low: 68, high: 80 }
};

const {today: {low: lowToday, high: highToday}} = LOCAL_FORECAST;
```

   <li>Use Destructuring Assignment to Assign Variables from Arrays</li>
  
```javascript
//swap variable
//usual method
let a = 8, b = 6;

let c = a;
a = b;
b = c;
  
console.log(a, b);

  
//Destructuring assignment
[a, b] = [b, a]

console.log(a, b);
```

   <li>Use Destructuring Assignment with the Rest Parameter to Reassign Array Elements</li>
  
```javascript
//Array.prototype.slice() 
//omit first two elements
const source = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
function removeFirstTwo(list) {
  const [, , ...arr] = list;  // can replace a and b with ",," => [,, ...arr]
  return arr;
}
const arr = removeFirstTwo(source);

console.log(arr)
```  
  
  <li>Use Destructuring Assignment to Pass an Object as a Function's Parameters</li>
  
```javascript
const stats = {
  max: 56.78,
  standard_deviation: 4.34,
  median: 34.54,
  mode: 23.87,
  min: -0.75,
  average: 35.85
};

const half = ({ max, min }) => (max + min) / 2.0; 

console.log(half(stats))
```  
  <li>Create Strings using Template Literals</li>

```javascript
const result = {
  success: ["max-length", "no-amd", "prefer-arrow-functions"],
  failure: ["no-var", "var-on-top", "linebreak"],
  skipped: ["no-extra-semi", "no-dup-keys"]
};
function makeList(arr) {
  "use strict";

  const failureItems = [];
  for (let i = 0; i < arr.length; i++) {
    failureItems.push(`<li class="text-warning">${arr[i]}</li>`);
  }
  return failureItems;
}

const failuresList = makeList(result.failure);
```

```javascript
// Alternative
const result = {
  success: ["max-length", "no-amd", "prefer-arrow-functions"],
  failure: ["no-var", "var-on-top", "linebreak"],
  skipped: ["no-extra-semi", "no-dup-keys"]
};
function makeList(arr) {
  "use strict";
  const failureItems = arr.map(item => `<li class="text-warning">${item}</li>`);
  return failureItems;
}
const failuresList = makeList(result.failure);
```

```
//output
[
  '<li class="text-warning">no-var</li>',
  '<li class="text-warning">var-on-top</li>',
  '<li class="text-warning">linebreak</li>'
]
```

<li>Write Concise Object Literal Declarations Using Object Property Shorthand</li>

```javascript
// returning an object that accepts the function’s parameters as its attributes.
const createPerson = (name, age, gender) => {
  "use strict";
  // change code below this line
  return {
    name,
    age,
    gender
  };
  // change code above this line
};
```

<li>Write Concise Declarative Functions with ES6</li>

```javascript
// With ES6, you can remove the function keyword and colon altogether when defining functions in objects

const bicycle = {
  gear: 2,
  setGear(newGear) {
    this.gear = newGear;
  }
};
bicycle.setGear(3);
console.log(bicycle.gear);
```

<li>Use class Syntax to Define a Constructor Function</li>

```javascript
// Explicit constructor
class SpaceShuttle {
  constructor(targetPlanet) {
    this.targetPlanet = targetPlanet;
  }
  takeOff() {
    console.log("To " + this.targetPlanet + "!");
  }
}

// Implicit constructor with no arguments
class Rocket {
  launch() {
    console.log("To the moon!");
  }
}

const zeus = new SpaceShuttle('Jupiter');
// prints To Jupiter! in console
zeus.takeOff();

const atlas = new Rocket();
// prints To the moon! in console
atlas.launch();
```
<li>Use getters and setters to Control Access to an Object</li>

```javascript
class Book {
  constructor(author) {
    this._author = author;
  }
  // getter
  get writer() {
    return this._author;
  }
  // setter
  set writer(updatedAuthor) {
    this._author = updatedAuthor;
  }
}
const novel = new Book('anonymous');
console.log(novel.writer);
novel.writer = 'newAuthor';
console.log(novel.writer);
```

<li>Use export to Share a Code Block</li>

```javascript
const add = (x, y) => {
  return x + y;
}

export { add, subtract };
```

<li>Create an Export Fallback with export default</li>

```javascript
// export default ==> usually used if only one value is being exported from a file.
// also used to create a fallback value for a file or module
// cannot use export default with var, let, or const

export default function add(x, y) {
  return x + y;
}

// anonymous fx
export default function(x, y) {
  return x + y;
}

```

<li>Import a Default Export</li>

```javascript
// imported value is not surrounded by { }
import add from "./math_functions.js";
```


</ol>


