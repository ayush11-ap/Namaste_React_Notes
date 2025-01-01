## Episode 3: Laying the Foundation 🚀

### 1. Running Programs 🏃‍♂️

- Whenever you don't know how to run a program, check the `package.json`. The `scripts` section will show you the commands.

```json
"scripts": {
    "start": "parcel index.html",    // Production build
    "build": "parcel build index.html" // Development build
}
```

- Example:
  ```bash
  npm run start === npm start
  ```

### 2. JSX ✨

- JavaScript syntax to create React elements.
- **JSX is not part of React.**
- JSX is not writing HTML inside JavaScript; it is an HTML-like or XML-like syntax.

### 3. Writing Code for Humans vs Machines

- Code is written primarily for **humans** because many developers will read it.
- Afterward, it is processed for machines.

### 4. Babel 🔧

- JSX code is transpiled before reaching the browser/JavaScript engine, managed by Parcel.
- Babel is a JavaScript compiler/transpiler.
- It converts code into a format that the JavaScript engine understands.
- Babel is a library, **not created by Facebook**.

### 5. React Code Conversion 🔄

1. React code is converted into `React.createElement`.
2. Transformed into a JavaScript object.
3. Finally, converted into an HTML element.

- In HTML: `class=""`
- In JSX: `className=""`

### 6. JSX Attributes 📝

- Use **camelCase** for attributes in JSX.

### 7. Multiline JSX Code 🖋️

- Wrap multiline JSX code in parentheses so Babel knows the start and end of the code.
  ```jsx
  const jsxHeading = <h1 className="head">Learning React 📍</h1>; // Implicit Return
  ```

### 8. Components in React 🏗️

#### Class-Based Component

- The **OLD** way to create components.
- Function name should start with a capital letter.

#### Functional Component

- The **NEW** way to create components.
- A normal JavaScript function that returns JSX.
  ```jsx
  const HeadingComponent = () => {
    return (
      <h1>
        📍➡️ A functional component is a normal JavaScript function that returns
        a piece of JSX code / React Element.
      </h1>
    ); // Explicit Return
  };
  ```
- **Rendering a component**: `<HeadingComponent />`

### 9. Component Composition 🔗

- Calling a functional component inside another functional component or nesting components is known as component composition.

- In `{}`:

  - Write any JavaScript logic or expressions.
  - Call functional components, e.g., `{HeadingComponent()}`.

- React allows:
  - Using React elements inside functional components.
  - Using functional components inside React elements.

### 10. Security in React 🔒

- React sanitizes code to prevent cross-site attacks or malicious actions, unlike plain JavaScript.

### 11. Function Calls in JSX 🔍

- Call a function inside JSX using curly braces `{}`.
- Write JavaScript code and perform logical operations.
  ```jsx
  {
    ComponentName();
  }
  ```
