## Build Javascript Objects
<ol>
  <li>Create object</li>
  
  Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through what are called properties. Objects are useful for storing data in a structured way
```javascript
const cat = {
  "name": "Whiskers",
  "legs": 4,
  "tails": 1,
  "enemies": ["Water", "Dogs"]
};
```
  <li>Accessing Object Properties with Bracket Notation & Dot Notation.</li>
  
```javascript
const myObj = {
  "Space Name": "Kirk",
  "More Space": "Spock",
  "NoSpace": "USS Enterprise"
};

myObj["Space Name"];
//Kirk
myObj.NoSpace;
//USS Enterprise
```
  
  <li>Accessing Object Properties with Variables.</li>
  
```javascript
const testObj = {
  12: "Namath",
  16: "Montana",
  19: "Unitas"
};
  
const playerNumber = 16; 
const player = testObj[playerNumber];
//Montana
```
  
  <li>Update Object Properties.</li>
  
```javascript
const myDog = {
  "name": "Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};

myDog["name"] = "Happy Coder"
```
  
  <li>Add New Properties to a JavaScript Object.</li>
  
```javascript
const ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};

ourDog.bark = "bow-wow";
```
  
  <li>Delete Properties from a JavaScript Object</li>
  
```javascript
delete ourDog.bark;
```
  
  <li>Using Objects for Lookups.</li>
  
```javascript
const alpha = {
  1:"Z",
  2:"Y",
  3:"X",
  4:"W",
  ...
  24:"C",
  25:"B",
  26:"A"
};

const thirdLetter = alpha[2];
//Y
const lastLetter = alpha[24];
//C
```
  
  <li>use the <b>.hasOwnProperty(propname)</b> method of objects to determine if that object has the given property name.</li>
  
```javascript
const myObj = {
  top: "hat",
  bottom: "pants"
};

myObj.hasOwnProperty("top");
//true
```
  
  <li>Accessing Nested Objects.</li>
  
```javascript
const myStorage = {
  "car": {
    "inside": {
      "glove box": "maps",
      "passenger seat": "crumbs"
     },
    "outside": {
      "trunk": "jack"
    }
  }
};

const gloveBoxContents = myStorage.car.inside["glove box"];
```
  
  
  
