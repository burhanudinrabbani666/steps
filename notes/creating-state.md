## Creating state

```js
export default function App() {
  const [step, setStep] = useState(1); // hooks

  console.log(step);
  function handlePrevious() {
    if (step > 1) setStep(step - 1);
  }

  function handleNext() {
    if (step < 3) setStep(step + 1);
  }
  return <div>{step}</div>;
}
```
