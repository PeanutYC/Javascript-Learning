# Promises in Javascript

* A promise in JavaScript is exactly what it sounds like - you use it to make a promise to do something, usually asynchronously. 
* When the task completes, you either fulfill your promise or fail to do so. 
* A promise has three states: pending, fulfilled, and rejected. 
* resolve is used when you want your promise to succeed, and reject is used when you want it to fail
* Promises are most useful when you have a process that takes an unknown amount of time in your code (i.e. something asynchronous), often a server request. 

<ol>
  <li>Create a JavaScript Promise</li>
  
```javascript
// Promise is a constructor function, so you need to use the new keyword to create one.
// It takes a function, as its argument, with two parameters - resolve and reject.
const makeServerRequest = new Promise((resolve, reject) => {
  
})

<li>Complete a Promise with resolve and reject</li>

```javascript
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer represents a response from a server
  let responseFromServer;
    
  if(responseFromServer) {
    resolve("We got the data");
  } else {  
    reject("Data not received");
  }
});
```

<li>Handle a Fulfilled Promise with then</li>

```javascript
// then method is executed immediately after your promise is fulfilled with resolve
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer is set to true to represent a successful response from a server
  let responseFromServer = true;
    
  if(responseFromServer) {
    resolve("We got the data");
  } else {  
    reject("Data not received");
  }
});

makeServerRequest.then(result => {
  console.log(result);
})
```

<li>Handle a Rejected Promise with catch</li>

```javascript
// catch is the method used when your promise has been rejected. It is executed immediately after a promise's reject method is called
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer is set to false to represent an unsuccessful response from a server
  let responseFromServer = false;
    
  if(responseFromServer) {
    resolve("We got the data");
  } else {  
    reject("Data not received");
  }
});

makeServerRequest.then(result => {
  console.log(result);
});

makeServerRequest.catch(error => {
  console.log(error);
})

```

</ol>



