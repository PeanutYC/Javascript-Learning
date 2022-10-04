### Recursion

```javascript
//for loop
function multiply(arr, n) {
  let product = 1;
  for (let i = 0; i < n; i++) {
    product *= arr[i];
  }
  return product;
}

//recursion
function multiply(arr, n) {
  if (n <= 0) {
    return 1;
  } else {
    return multiply(arr, n - 1) * arr[n - 1];
  }
}
```

<ol>
  <li>Use Recursion to Create a Countdown.</li>
  
```javascript
function countdown(n){
  if (n < 1){
    return [];
  } else {
    let countArray = countdown(n - 1);
    //adds the element at the beginning of the array
    countArray.unshift(n);
    return countArray;
  }
}

console.log(countdown(10))
//[10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
 
```

```javascript
// Alternative 1
function countdown(n) {
  if (n < 1) {
    return [];
  } else {
    const arr = countdown(n - 1);
    arr.splice(0, 0, n);
    return arr;
  }
}
```
```javascript
//Alternative 2
function countdown(n){
   return n < 1 ? [] : [n].concat(countdown(n - 1));
}
```

<li>Use Recursion to Create a CountUp.</li>
  
```javascript
function countup(n) {
  if (n < 1) {
    return [];
  } else {
    const countArray = countup(n - 1);
    countArray.push(n);
    return countArray;
  }
}
console.log(countup(5));
//[1, 2, 3, 4, 5]
 
```

<li>Use Recursion to Create a Range of Numbers.</li>
  
```javascript
function rangeOfNumbers(startNum, endNum) {
  if (endNum < startNum) {
    return [];
  } else {
    const numbers = rangeOfNumbers(startNum, endNum - 1);
    numbers.push(endNum);
    return numbers;
  }
}
```
```javascript
// Alternative
function rangeOfNumbers(startNum, endNum) {
  return endNum < startNum
    ? []
    : rangeOfNumbers(startNum, endNum - 1).concat(endNum);
}
```
</ol>
