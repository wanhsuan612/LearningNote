## React Hooks API

### `useEffect`
-----------------------
* Do something after render.
* `useEffect` takes two arguments. The first one is a function, and the second one is an array of dependency arguments. useEffect will listen to the value of dependency arguments, and do the function.

```
useEffect(() => {
    setCount(a);
}, [a])
```
### `useState`
-----------------------
* Create a function component and give it a state.
* `useState` will return a state variable and a function to update the state.
* When the state changed, it will trigger re-render.
```
const [count, setCount] = useState(0);
```