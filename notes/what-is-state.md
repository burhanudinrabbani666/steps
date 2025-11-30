## What is State

source:
[UseState](https://react.dev/reference/react/useState)

Data that a component can hold **over time**, necessary for information that it needs to **remember** throughout the apps lifecycle

**"component's Memory"** 🧠

```jsx
const [state, setState] = useState(initialState);
```

**state** variable / piece of state: A single variable on a component(component state)

updateing **component state** triggers React to **re-render the component**.

### State allowes developers to:

1. Update the components view / UI (by re-rendering it)
2. Persist local variables between renders
