## 🌟 **Episode 9: Optimising Our App** 🌟

    - 📚 **Single Responsibility Principle**
    - 🔄 **Reusable**, 🛠️ **Maintainable**, 🧪 **Testable**.
    - 🧩 Every function or component should have **one single responsibility**.

    ---

    - ⚙️ **Hooks**
    - 🪝 A hook is essentially a **utility function**.
    - 🛠️ **Custom Hooks**:
    - ✅ Always start the name with `use` (e.g., `useCustomHook`) as a **best practice**.

    ---

    - 🚀 **Performance Optimisation Techniques**
    - ✂️ **Chunking**
    - 🗂️ **Code Splitting**
    - 📦 **Dynamic Bundling**
    - 💤 **Lazy Loading**
    - 🖱️ **Dynamic Loading**
    - All these techniques help make code **concise** and **divide it into smaller chunks**, improving **website loading speed**.
    - 🔄 **Lazy Loading/On-Demand Loading**: Components are loaded only when **user demand** occurs.

    ---

    - 💤 **lazy() Function**
    - 📦 Provided by the React package to **load components on demand**.
    - 🖋️ **Usage**:
    ```javascript
    import { lazy } from "react"; // Named import
    const About = lazy(() => import("./About")); // Callback function
    ```

    ---

    - ⏳ **Suspense Component**
    - 🚀 Used to show a **loader** while a component is **loading**.
    - 🔒 **Wrap lazy components inside Suspense**.
    - 🖋️ **Example**:
    ```jsx
    <Suspense fallback={<h1>Loading...</h1>}>
        <About />
    </Suspense>
    ```
    - 🌟 You can also pass a **shimmer UI** or custom loader as `fallback`.

    ---
