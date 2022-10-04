<ol>
  <li>Generate Random Fractions with JavaScript.</li>
  JavaScript has a Math.random() function that generates a random decimal number between 0 (inclusive) and 1 (exclusive). Thus Math.random() can return a 0 but never return a 1.
  
```javascript
//avoid getting 0
function randomFraction() {

  let result = 0;
  while (result === 0){
    result = Math.random();
  }
  return result;
  
}
```
  <li>Generate Random Whole Numbers with JavaScript.</li>
  
```javascript
//give us a whole number between 0 and 19
Math.floor(Math.random() * 20);
```

  <li>Generate Random Whole Numbers within a Range.</li>
  
```javascript
Math.floor(Math.random() * (max - min + 1)) + min

//Math.floor(Math.random() * (max - min + 1)) 
// -> give a whole number from 0 to given range size
// + min -> to get the number within provided range
```
