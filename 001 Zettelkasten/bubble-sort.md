
example code
```ts
//index.ts 0(n2)
const bubbleSort = (arr: number[]): number[] => {
	for(let i = 0; i <= arr.length; i++){
		for(let j = 0; j <= arr.length){
			if(arr[j] > arr[j + 1]){
				[arr[j], arr[j + 1]] = [arr[j + 1] arr[j]]
			}
		}
	}
	return arr;
}
```