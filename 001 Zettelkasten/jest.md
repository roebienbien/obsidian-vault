2023-12-20 05:41

Status: #idea

Tags: [[programming]]

# jest
Jest is a delightful JavaScript Testing Framework with a focus on simplicity.

How to: 
```js
//index.js
function sum(a, b){
	return a + b;
}

module.export = sum;
```

Then create  a file named`sum.test.js`:
```js
//sum.test.js
it("adds 1 + 2 to equal 3", () => {
	expect(sum(1, 2)).toBe(3);
})
```

finally, run `npm run test` after writing it in the package.json under the script object

