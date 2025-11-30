## Dont set state manually

React is all about immutability

A component’s props and state are immutable snapshots. Never mutate them directly. Instead, pass new props down, and use the setter function from useState.

```jsx
// const [test] = useState({ name: "Bani" });
const [test, setTest] = useState({ name: "Burhanudin" });

// Bad Practice ❗
// test.name = "Burhanudin";
// Good Prectice ✅
setTest({ name: "Rabbani" });
```

### Invalid ❗

```js
// ❌ Array push mutation
function Component() {
  const [items, setItems] = useState([1, 2, 3]);

  const addItem = () => {
    items.push(4); // Mutating!
    setItems(items); // Same reference, no re-render
  };
}

// ❌ Object property assignment
function Component() {
  const [user, setUser] = useState({ name: "Alice" });

  const updateName = () => {
    user.name = "Bob"; // Mutating!
    setUser(user); // Same reference
  };
}

// ❌ Sort without spreading
function Component() {
  const [items, setItems] = useState([3, 1, 2]);

  const sortItems = () => {
    setItems(items.sort()); // sort mutates!
  };
}
```

### Valid ✅

```js
// ✅ Create new array
function Component() {
  const [items, setItems] = useState([1, 2, 3]);

  const addItem = () => {
    setItems([...items, 4]); // New array
  };
}

// ✅ Create new object
function Component() {
  const [user, setUser] = useState({ name: "Alice" });

  const updateName = () => {
    setUser({ ...user, name: "Bob" }); // New object
  };
}
```
