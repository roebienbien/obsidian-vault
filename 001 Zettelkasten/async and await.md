2023-12-13 21:07

Status: #idea

Tags: [[programming]]

# async and await
"Async and await make promises easier to read and write"
- `async` makes a function return a promise
- `await` makes a function wait for the promise

ECMAScript 2017 introduced the JavaScript keywords async and await.

```js
//index.js
const myTimeout = async () => {
  let myPromise = new Promise((resolve) => {
    setTimeout(() => resolve('Timeout test!'), 3_000); // wait for 3 seconds
  });
  document.getElementById('demo').innerHTML = await myPromise;
};

myTimeout();

```





# References
[JavaScript Async/Await](https://www.w3schools.com/js/js_async.asp)