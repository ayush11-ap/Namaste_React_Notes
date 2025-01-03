## Episode 5: Let's Get Hooked 🪝

### 1. 📚 Libraries and Frameworks

- Enhance the developer experience by enabling you to write less code and achieve more functionality on the webpage.

### 2. ❌ Avoid Hard-Coded Strings

- Never keep hard-coded strings inside a component (e.g., URLs).
- **Best Practice**: Store hard-coded data in a separate file and import it into the main file.
  ```javascript
  // utils/constant.js
  export const CDN_URL = "https://api.com";
  ```
- Follow **camelCase** for file names and **SNAKE_CASE** for variables.

### 3. 🔄 Export and Import

- Export and import components and utilities for reuse.
  #### Export:
  - **Single Export**:
    ```javascript
    function Card() {}
    export default Card;
    ```
  - **Named Export**:
    ```javascript
    export function Add() {}
    export function Remove() {}
    ```
  #### Import:
  - **Single Import**:
    ```javascript
    import Card from "./fileName.jsx";
    ```
  - **Named Imports**:
    ```javascript
    import { Add, Remove } from "./fileName.jsx";
    ```
- **Q**: Can default and named imports coexist in the same file?
  **A**: Yes, both can be used together without errors.

### 4. 🔠 Component Best Practices

- Keep component file sizes under **100 lines**.
- Split large components into smaller components for better readability and maintainability.
- **Why React is Efficient**: React is designed for fast and efficient DOM manipulation.

### 5. 💪 State Variable (`useState`)

- `useState` provides a state variable and a setter function:
  ```javascript
  const [val, setVal] = useState({ name: "Ayush" });
  ```
- **Array Destructuring** Example:
  ```javascript
  const arr = useState({ name: "Ayush" });
  const [val, setVal] = arr;
  ```
- **Key Features**:
  - The initial state is assigned to `val`.
  - `setVal` updates the `val` and triggers React's Reconciliation Algorithm.
  - React re-renders the component whenever a state variable is updated.
  - Syncs data with the UI automatically.

### 6. 🔧 React Hooks

- React Hooks are normal JavaScript functions provided by React with specific purposes.
- **`useState()`**:
  - Keeps data in sync with the UI.
  - Facilitates efficient DOM manipulation.

### 7. 🎮 React Behind the Scenes

- React uses the **Reconciliation Algorithm** (React Fiber) to update the DOM efficiently.
- Maintains a **Virtual DOM**, a lightweight representation of the actual DOM.
- **Diff Algorithm**:
  - Compares the old Virtual DOM with the new Virtual DOM.
  - Updates only the changed parts in the actual DOM.
- **React Fiber**:
  - Core algorithm introduced in React 16.
  - Optimizes rendering for modern applications.
  - More details: [React Fiber Architecture](https://github.com/acdlite/react-fiber-architecture).

### 8. ⚡ Why React is Fast

- Efficient Virtual DOM manipulations.
- Diff Algorithm for comparing and updating the DOM.
- Reconciliation Algorithm for syncing UI with state changes.

### 9. 🔅 Identifying Hooks

- Any React element with a name starting with `use` is a Hook.
