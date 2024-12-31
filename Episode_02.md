## Episode 2: Igniting Our App 🚀

### 📦 npm

- `npm` doesn’t officially stand for "node package manager"; it can mean anything fun like "neverending prototype mode" or "nesty pizza manager." 🍕
- While npm manages packages, it doesn’t have a definitive full form.

### Steps:

1. `npm init`:
   - Write description.
   - Test command: `jest`.
   - Git repository.
   - Keywords: Any word.
   - Author: **OUR NAME**.
   - License.
   - Creates `package.json` file.
2. `npm install -D parcel`: Installs Parcel as a devDependency (bundler).
3. `npx parcel index.html`: Runs Parcel.
4. `npm install react react-dom`: Installs React and React DOM.

### 📄 package.json

- Configuration file for npm.
- Tracks the versions of installed packages. 📜
- Supports caret (`^`) and tilde (`~`) for version control.

### Bundler

- Bundles or packages the app for production.
- Examples: Parcel, Webpack, Vite.

### 🎯 Caret (^) and Tilde (~)

- **Caret (`^`)**: Updates minor versions automatically.
  - Example: `^2.3.3` can update to `2.3.4`. 🔄
- **Tilde (`~`)**: Updates major versions automatically.
  - Example: `~2.3.3` can update to `3.0.0`. 🚀
- Recommended to use caret (`^`) as major updates might break the code. ⚠️

### 🔗 Types of Dependencies

1. **devDependencies**: Required during development. 💻
2. **Dependencies**: Used in production. 🌐

### 📦 Parcel

- Parcel is a bundler. 📦
- Install using `npm install -D parcel` (adds as devDependency). ⚙️

### 🔒 package-lock.json

- Tracks exact versions of installed packages. 📌
- Contains exact versions of transitive dependencies. 🔄

### 📜 package.json vs package-lock.json

- **package.json**: Keeps approximate versions of packages.
- **package-lock.json**: Tracks exact versions.

### Node Modules

- Acts like a database where all packages are stored.
- Collection of installed packages.

### 🔄 Transitive Dependencies

- Dependencies that have their own dependencies, forming a dependency tree.
- Example: `node_modules`. 📚

### 📜 Package Files

- Each dependency has its own `package.json` and `package-lock.json`. 🗂️

### 🚀 NPX

- Used to execute any package directly.
- Command: `npx <packageName>`.
- A tool for running Node.js packages, scripts, and binaries without global installation.

### 📦 Parcel: The Ultimate Bundler

Parcel offers features to streamline development and optimize web projects:

- **Dev Build & Local Server**: Quickly set up environments.
- **HMR (Hot Module Replacement)**: Update modules without a full refresh.
- **File Watching Algorithm**: Efficient monitoring via C++.
- **Caching**: Faster builds through caching mechanisms.
- **Image Optimization**: Reduce image sizes for faster loads.
- **Minification**: Compress code to reduce file sizes.
- **Bundling**: Combine multiple files into one.
- **Compression**: Removes whitespace for optimal performance.
- **Consistent Hashing**: Stable hashed filenames for caching.
- **Code Splitting**: Load only the necessary code for faster initial load.
- **Differential Bundling**: Supports older browsers with appropriate bundles.
- **Diagnostics & Error Handling**: Built-in debugging tools.
- **HTTPS**: Secure your local development server.
- **Tree Shaking**: Removes unused code for better performance.

#### Production Build

- Run: `npx parcel build index.html`
- Remove "main": "script.js" from `package.json` to avoid errors.

### GitHub Best Practices

- Don’t upload `.parcel-cache`, `dist`, or `node_modules` as they can be regenerated.

### 🤔 Why is React Fast?

- React is optimized for performance using bundlers like `Parcel` for efficient rendering and updates.

### 📜 Browserslist Configuration

In `package.json`, specify target browsers:

```json
{
  "dependencies": {
    "...": "..."
  },
  "browserslist": ["last 1 Chrome version", "last 2 Firefox versions"]
}
```

- Ensures compatibility with specified browser versions.
- For more details, visit [browserslist.dev](https://browserslist.dev).
- Country-specific configuration: Read [this GitHub repo](https://github.com/browserslist/browserslist#query-composition).
