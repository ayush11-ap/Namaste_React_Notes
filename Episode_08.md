# Class-Based Components in React: A Journey into the Past 🎩

Welcome, fellow traveler, to the realm of React! Today, we shall embark on a quest to explore the ancient artifacts known as **Class-Based Components (CBC)**. Fear not; these components may lack the sleekness of their functional counterparts, but they carry tales of yore and wisdom from React's earlier days. 📜✨

## 1. The Noble Class-Based Component

### What Is It?

- A **Class-Based Component** (CBC) is like a venerable sage—a JavaScript class that extends `React.Component`.
- Its sacred duty? To render a piece of JSX code, much like a medieval minstrel performing for the court.
- In simpler terms, it's an older way of defining React components.

### The Ancient Incantation:

```jsx
class MyComponent extends React.Component {
  render() {
    return <h1>Class-Based Component</h1>;
  }
}
```

- Behold! Our noble `MyComponent` stands tall, ready to weave its JSX magic.

### Why the `super(props)` Incantation?

- Fear not the cryptic `super(props)` within the constructor!
- It's a ritual—a way to call upon the constructor of the parent class (the mighty `React.Component`).
- By invoking `super(props)`, we gain access to the parent's properties and methods. 🪄

## 2. The State: A Treasure Trove of Variables

### The State Object:

- Picture a grand chest—the **state object**—containing all our precious variables.
- Within its wooden confines:
  ```jsx
  this.state = {
    count: 0,
    count2: 2,
  };
  ```
  - These are our apples—`count` and `count2`.
  - But beware! Never update state variables directly using the assignment operator. 🍎

### Updating the State:

- To alter our apple count, we invoke the sacred `setState({ stateVariable })`:
  ```jsx
  <h1>Count: {count}</h1>
  <button onClick={() => {
      this.setState({
          count: this.state.count + 1,
          count2: this.state.count2 + 1,
      });
  }} className='border rounded-lg'>
      Count Increase
  </button>
  ```
  - With each button click, our apples multiply. 🌿🍏

### The Life Cycle of a Class-Based Component:

1. **Mounting the CBC**:

   - The CBC dons its armor and prepares for battle.
   - Constructor fires up, creating a new instance of the class.
   - Render method paints the shield and sword (i.e., JSX).
   - `componentDidMount` raises the banner high—a signal that the CBC is ready for action.

2. **Unmounting the CBC**:

   - When we ride to distant lands (i.e., navigate away), `componentWillUnmount` sounds the retreat.
   - The CBC sheathes its sword and rests.

3. **Children's Life Cycle**:
   - Imagine a royal procession:
     - Parent Constructor
     - Parent Render
       - First Child Constructor
       - First Child Render
       - Second Child Constructor
       - Second Child Render
       - First Child `componentDidMount`
       - Second Child `componentDidMount`
     - Parent `componentDidMount`

### In-Depth Exploration:

- Never compare life cycle methods with functional components (those `useEffect` wizards).
- Remember: On the first render, `componentDidMount` is called. Subsequent renders update it; they don't remount it.
- Always use `componentWillUnmount` to avoid repeated `componentDidMount` calls during navigation.

### 🌟 Bonus Quest:

- For those seeking enlightenment, watch the extra live session (a mere 47 minutes, but oh, the wisdom!)—worth every pixel. 📺🔮

And thus, our journey through the annals of React comes to an end. May your components be as sturdy as castle walls and your state variables as abundant as a dragon's hoard! 🏰🐉✨

Feel free to share more riddles or embark on new quests—I'm here, ready to unravel them all! 🤓🌟🛡️
[Learn more about React Class Components](https://reactjs.org/docs/react-component.html) 📖🔗!
[Explore the Children's Lifecycle Methods](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/) 📊🔗!
