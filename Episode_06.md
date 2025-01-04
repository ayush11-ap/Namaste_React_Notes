# Episode 6: Exploring the World 🌍

1. **Monolith Architecture**:  
   This architecture combines the API, frontend, backend, authentication, and database into a single application. 🏢 Everything is interconnected, making it simpler but less flexible for scaling and updates.

2. **Microservices Architecture**:  
   Here, each functionality like API, frontend, backend, authentication, and database is separated into individual services. 🛠️🔗 This approach follows the principles of separation of concerns and single responsibility, providing flexibility and scalability. In today's world, microservices are becoming the norm.

   - **Example**: We are creating UI Microservices, and microservices are written in various languages like React (UI), Backend (Java), Database (MySQL), etc.

3. **Load ➔ Render ➔ API ➔ Render**:  
   This sequence illustrates the process of loading a page, rendering the initial UI, fetching data from an API, and then rendering the updated UI. 🔄

4. **useEffect(callback, [dependencies])**:

   - `useEffect` is a hook that takes a callback function and an array of dependencies. The callback runs after the component is rendered. 📅
   - **Example**:
     ```javascript
     useEffect(() => {
       console.log("useEffect Called");
     }, []);
     ```
   - This hook helps manage side effects like fetching data or setting up subscriptions.
   - First, the body of the component is rendered, and after that, `useEffect` is called.

5. **fetch()**:  
   This is a powerful function provided by the browser's JS engine to fetch data from a server. 🌐📬 It enables asynchronous operations, making web applications dynamic and interactive.

6. **Shimmer UI**:  
   Instead of using traditional loaders like GIFs, images, or videos, modern applications use `Shimmer UI`. ✨🚫🖼️ This technique provides a skeleton screen that mimics the page's layout, enhancing user experience during data loading.

7. **Conditional Rendering**:  
   This involves rendering components based on certain conditions. 🔄❓ It ensures that only the necessary components are displayed, optimizing performance and user experience.  
   **Example**:

   ```javascript
   if (listOfRestaurant.length === 0) {
     return <Shimmer />;
   }
   ```

8. **Component Re-rendering**:  
   When a small change occurs in a component, the entire component re-renders. However, only the changed code is updated, while the rest remains the same. 🔄🖥️ React efficiently manages these updates to maintain performance.

9. **State Updates and Reconciliation**:  
   Whenever a state variable updates, React triggers a reconciliation cycle, re-rendering the component. 🔄 This process ensures the UI is in sync with the state changes.

   - Whenever a state variable updates, React triggers a reconciliation cycle (re-renders the component).

10. **React Fiber**:  
    The new reconciliation algorithm in React, called Fiber, efficiently finds differences between two virtual DOMs (new VD and old VD) and updates the modified code only. ⚡🌐 It updates only the changed parts of the component, making React fast and responsive. This behind-the-scenes optimization is key to React's performance.

React's efficient handling of state changes, component updates, and rendering processes ensures a smooth and dynamic user experience.
