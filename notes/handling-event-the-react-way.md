## Handling Event in react way

```jsx
function App() {

  function handleNext(){ // have function inside function
    console.log("hello") // this for logic in this component
  }

  return(
  <button
    style={{ backgroundColor: "#7950f2", color: "#fff" }}
    onClick={handleNext} // inline event handle
  >
    Next
  </button>;
  )
}
```
