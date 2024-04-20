2023-12-12 16:37

Status: #idea

Tags: [[programming]]

# callbacks
**"I will call back later!"**, A call back is a function passed as an argument to another function
```jsx
function myDisplayer(content){
	document.getElementById("demo").innerHTML = content;
}

function myCalculator(num1, num2, myCallback){
	let sum = num1 + num2;
	myCallback(sum)
}

myCalculator(5,5, myDisplayer)
```






# References
