## Episode 4: 🎓 Talk Is Cheap, Show Me The Code

### 1. Inline CSS in React 🎨

- Use inline CSS in React by providing the `style` attribute as an object:

  ```jsx
  const styleCard = {
    backgroundColor: "green",
  };

  const RestaurantCard = () => {
    return (
      <div className="res-card" style={styleCard}>
        <h1>Ayush Food's Center</h1>
      </div>
    );
  };
  ```

### 2. 🧩 Functional Components

- At its core, a functional component is just a regular JavaScript function.
- **Props** are simply arguments passed to this function, wrapped by React in an object.

#### Key Points About Props:

- Props are passed as an object.
- **Props Are Immutable**: Once set, `props` cannot be changed.

### 3. 🛠️ Config-Driven UI

- Create a UI dynamically based on a provided configuration.
- Keep configurations in one place, and the UI is generated based on them.

#### Benefits of Config-Driven UI:

- 📍 Location-Based Config: Customize UI dynamically based on user location.
- 📦 Reusability: Centralized changes make the UI scalable and reusable.

#### Using Props Properly:

    ```jsx
    const RestaurantCard = (props) => {
        const { resData } = props;
        return (
            <div className="res-card">
                <h1>{resData.name}</h1>
            </div>
        );
    };

    const resObj = { name: "Ayush Food's Center" };
    <RestaurantCard resData={resObj} />;
    ```

### 4. 🔑 Keys in Lists

- When using the `map()` function to iterate over an array, always pass a unique `key` to the parent element.
- **Why?** Helps React efficiently identify and update elements.

#### ❌ Avoid Index as Key:

- Do not use the array index as a key unless no unique ID is available.
