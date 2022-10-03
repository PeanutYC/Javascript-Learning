<ol>
  <li>Find the length of a String value by writing <b>.length</b> after the string variable or string literal.</li>
  
```javascript
// Setup
let lastNameLength = 0;
const lastName = "Lovelace";

lastNameLength = lastName.length;
```
  <li>Bracket notation is a way to get a character at a <b>specific index</b> within a string.</li>
  
```javascript
// Setup
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
</ol>
