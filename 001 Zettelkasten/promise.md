2023-12-13 02:17

Status: #idea

Tags:

# promise
"I promise a result!", A Promise is a javascript object that links producing code(takes time) and consuming code(waiting for producing code).


## Promise Object
The promise object has two callbacks the:

| Results | Callback|
| ---- | ---- |
| Success | resolve(value)|
| Error | reject(value)|

## Promise Object Properties

| Results | Callback| 
| ---- | ---- |
| pending | undefined|
| fulfilled | a result value|
| rejected | an error object|

``` js
function myDisplayer(some) {
  document.getElementById('demo').innerHTML = some;
}

// producing code
let myPromise = new Promise((resolve, reject) => {
  let x = 200;
  if (x === 200) resolve('OK');
  else reject('ERROR');
});

// consuming code
myPromise.then(
  (value) => myDisplayer(value),
  (error) => myDisplayer(error)
);

```






# References
