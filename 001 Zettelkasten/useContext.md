2024-10-21 14:30

Status: #idea

Tags:  [[react-hooks]]

# useContext

is a React hooks used for passing props between components without using prop drilling.
It has Provider and Consumer

outline
- [ ] import useContext();
- [ ] Create context :
 ```tsx
export interface IProduct {
	// code here
}

// create Product object to be passed as value
const Product = {
	//code here
}

const ProductsContext = createContext<IProduct[]>([]);

// create a custom hook
export const useProductContext = () => {
	const product = useContext(ProductsContext);
	// catch if undefined
	if(product === undefined){
		throw new Error('value must not be undefined')
	}
	return product;
}

// return a parent component that wraps the children with provider
export default function ProductsProvider({children}: {children: React.ReactNode}) {
	return(
		<ProductsContext.Provider value>{children}</ProductsContext.Provider>	
	)	
}
 ```

- [ ] create Parent Component that wraps the children component with `ProductsProvider`: 
```tsx
export default function ProductDashboard(){
	return(
		<ProductsProvider>
			<ProductPage />
		</ProductsProvider>	
	)
}
```
- [ ] Create Child Component: 
```tsx
export default function ProductPage(){
	const product = useProductContext();
	return(
	//code here	
	)
}
```

