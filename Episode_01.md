## Episode 1: Inception 🌟

1. **Creating a React Element in HTML using React CDN** 🏗️
    ```html
    <div id="root"></div>
    <script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
    ```

    ```javascript
    let heading = React.createElement("element", { id: "root" }, "data to be inserted in element");
    console.log(heading); // This is a React element and it is an object.

    let heading = React.createElement("div", {id:"parent"}, 
        React.createElement("div", {id:"child"}, 
            [ 
                React.createElement("h1", {id:"tag"}, "I'm h1 tag"), 
                React.createElement("h2", {id:"tag"}, "I'm h2 tag"),
            ]
        )
    );
    ```
    To pass elements in the form of siblings, write them in an array - `[]`.

    React is a JavaScript library.
    - React element is a plain JavaScript object.
    - When rendered on the DOM, it is converted into an HTML element.

2. **Creating Root** 🌳
    ```javascript
    ReactDOM.createRoot(document.getElementById("root")).render(heading);
    // The render() method converts the heading (which is an object) into an HTML element and inserts it into the root element.
    ```

3. **Props** 📦
    - Props are the attributes and children present inside an element.
