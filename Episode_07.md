## Episode 7: Finding The Path: About Routing 🛣️, Hooks like useState & useEffect

    1. useEffect(callback, [dependency]):
    - Whenever the component is rendered, `useEffect` is called. If the dependency array is empty, `useEffect` is called only once. If the dependency array has values, `useEffect` is called whenever any of those values change. 🔄📅
        - `dependency` is not mandatory in `useEffect`. If not provided, `useEffect` is called every time the component is rendered. 🔄📅
        - An empty dependency array ensures `useEffect` is called only once. 🔄📅
        - If the dependency array contains values, `useEffect` is called whenever those values update. 🔄📅

    2. useState():
    - Do not create `useState` outside your component. 🚫 Avoid creating `useState` inside conditional statements, loops, or functions. ❌🔁
        ```javascript
        // Incorrect usage
        for() {
            const [name, setName] = useState("Ayush");
        }

        if() {
            const [name, setName] = useState("Ayush");
        }

        function xyz() {
            const [name, setName] = useState("Ayush");
        }
        ```
    - `useState` is used to create local variables in your functional component. 📦 Call it at the top of your component. 🔝

    3. react-router-dom:
    - Used for navigating between multiple pages in a React application. 🛤️
    - Install with `npm i react-router-dom`. 📦
    - `createBrowserRouter` and `RouterProvider` configure routing in your app. ⚙️
    - `Outlet` is a component that gets filled by the child components of a route. Behind the scenes, it converts into the component of that route in the HTML. 🧩
    - To create routes:
        ```javascript
        import { createBrowserRouter, RouterProvider, Outlet } from 'react-router-dom';

        const AppLayout = () => {
            return (
                <div className='app'>
                    <Header />
                    <Outlet />  // Children components of the route are filled here.
                </div>
            );
        };

        const appRouter = createBrowserRouter([
            {
                path: '/',
                element: <AppLayout />,
                children: [
                    {
                        path: '/',
                        element: <Body />
                    },
                    {
                        path: '/about',
                        element: <About />  // /about path shows About component
                    },
                    {
                        path: '/contact',
                        element: <Contact />
                    }
                ],
                errorElement: <Error />  // Path not found shows Error component
            },
        ]);

        // Provide routing configuration to our app.
        root.render(<RouterProvider router={appRouter} />);
        ```

        - wherever u see `use` before any variable it's a hook.

    - `useRouteError`: A hook provided by `react-router-dom` that gives more data related to routing errors. 🚨
    - Never use `<a></a>` tags to link pages in React because they refresh the page and cause a full re-render. Use `Link` instead, which is provided by `react-router-dom`: 🔗🚫
        ```javascript
        import { Link } from 'react-router-dom';
        <Link to='/about'>About</Link>
        ```
    - Behind the scenes, `Link` is converted to an `<a href="#"></a>` tag. 🔗

    4. Types of Routing:
        - Client-Side Routing in React 16

    1. Definition: Routing is managed in the browser using React components.
    2. Location: Routes are handled within the React application.
    3. URL Handling: React Router manages URL changes without full page reloads.
    4. Page Loading: Only the components associated with the route are re-rendered.
    5. Performance: Fast transitions since only parts of the UI are updated.
    6. Example: Using `react-router-dom` for routing.
    - Basic Setup:
        ```jsx
        import React from 'react';
        import { BrowserRouter as Router, Route, Switch } from 'react-router-dom';

        const Home = () => <h2>Home Page</h2>;
        const About = () => <h2>About Page</h2>;

        function App() {
        return (
            <Router>
            <Switch>
                <Route path="/" exact component={Home} />
                <Route path="/about" component={About} />
            </Switch>
            </Router>
        );
        }

        export default App;
        ```

        - Server-Side Routing with React 16

    1. Definition: Routing is managed by the server and serves different HTML pages based on the route.
    2. Location: Routes are handled on the server before sending a response to the client.
    3. URL Handling: Each URL request results in a new page load from the server.
    4. Page Loading: The server provides the full HTML page for each route.
    5. Performance: Slower transitions due to complete page reloads.
    6. Example: When using server-side rendering (SSR) with frameworks like Next.js.
    - Basic Setup in Next.js:
        ```jsx
        // pages/index.js
        export default function Home() {
        return <h1>Home Page</h1>;
        }

        // pages/about.js
        export default function About() {
        return <h1>About Page</h1>;
        }
        ```


    5. useParams:
    - The `useParams` hook in React Router is used to access URL parameters in a component. It returns an object of key-value pairs where the key is the parameter name and the value is the parameter value. 🗺️🔑
