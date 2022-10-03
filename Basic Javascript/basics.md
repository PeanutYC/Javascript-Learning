<ol>
  <li>Find the length of a String value by writing <b>.length</b> after the string variable or string literal.</li>
  
```javascript
let lastNameLength = 0;
const lastName = "Lovelace";

lastNameLength = lastName.length;
```
  <li>Bracket notation is a way to get a character at a <b>specific index</b> within a string.</li>
  
```javascript
let firstLetterOfLastName = "";
const lastName = "Lovelace";

firstLetterOfLastName = lastName[0];
```
  <li>In order to get the <b>last letter</b> of a string, you can subtract one from the string's length.</li>
  
```javascript
const firstName = "Ada";
const lastLetter = firstName[firstName.length - 1];
```
  <li>retrieve the <b>Nth-to-last character</b>.</li>
  
```javascript
const firstName = "Augusta";
const thirdToLastLetter = firstName[firstName.length - 3];
```
  <li>Access Multi-Dimensional Arrays With Indexes.</li>
  
```javascript
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];
  
const subarray = arr[3];
// [[10, 11, 12], 13, 14]
const nestedSubarray = arr[3][0];
// [10, 11, 12]
const element = arr[3][0][1];
// 11
```
  <li><b>append data</b> to the end of an array is via the <b>push()</b> function.</li>
  
```javascript
const arr1 = [1, 2, 3];
arr1.push(4);
// [1, 2, 3, 4]
  
const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
// ["Stimpson", "J", "cat", ["happy", "joy"]]
```
  
   <li><b>.pop()</b> removes the last element from an array and returns that element.</li>
  
```javascript
const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();
console.log(oneDown);
//6
console.log(threeArr);
//[1, 4]
```
  <li><b>.shift()</b> removes the first element instead of the last.</li>
  
```javascript
const ourArray = ["Stimpson", "J", ["cat"]];
const removedFromOurArray = ourArray.shift();
//Stimpson
```
  <li><b>.unshift()</b> adds the element at the beginning of the array.</li>
  
```javascript
const ourArray = ["Stimpson", "J", "cat"];
ourArray.unshift("Happy");

//["Happy", "Stimpson", "J", "cat"]
```
</ol>
