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
  const [a, b, ...arr] = list; 
  return arr;
}
const arr = removeFirstTwo(source);

console.log(arr)
```  
  
</ol>
