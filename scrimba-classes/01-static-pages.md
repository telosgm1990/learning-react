# Static pages classes

## 1. References

1. https://stackoverflow.com/a/31520672/26058659
2. https://github.com/coreybutler/nvm-windows
3. https://github.com/coreybutler/nvm-windows/releases
4. https://stackoverflow.com/a/66951910/26058659
5. https://stackoverflow.com/a/56121123/26058659
6. https://react.dev/learn/creating-a-react-app#react-router-v7
7. https://www.freecodecamp.org/news/npm-vs-npx-whats-the-difference/
8. https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement

## 2. Notes

### 2.1. Course Introduction

- The comparison between playing an instrument and to program is so real. I have a "problem" that I wanna to learn any tech tool/language at same time I wanna to put in the "best" way. I love clean code, to organize/refactor my projects, but this is stucking some how....So I liked the idea of this kind of tutorial, and I need to practice, to learn, forgettin about optimizing, best patterns, etc...

### 2.2. What we'll learn

Nothing special here, just they showing the course content.

### 2.3. First React Code

> **INFO** I am using Windows to run this project, so any command, process showed below is relative to this OS.

- Amazing! The "video" shares the same editor with me. How do they do that? 
- Instead of writing the code on Scrimba, I will try to replicate their code here in VSCode;
- First, I am installing the `react` and `react-dom` dependencies via `npm`;
- Updated my local `npm` version by running:<sup>[1](#1-references)</sup>

```powershell
npm install -g npm
```

- Installed the `nvm-windows` tool. This tool helps manage multiple installations of node.js;<sup>[2,3](#1-references)</sup>
- Installed the most recent LTS version for node by running:

```powershell
nvm install lts
nvm use lts
```

> **IMPORTANT** At the time I am writing this, the LTS version was **22.17.0**.

- Initialized project by running the command below.

```powershell
npm init
```

- Copied the code from scrimba to this project;
- Changed the paths in `index.html` from `/...` to `./...`. In scrimba it looks like the project run at root folder in some environent. Changing to `./`, indicates to interpreter that other files are in same folder, not necessary in root folder;
- I've tried to open the `index.html` using my local browser, and the console logged this CORS error message:

```js
Access to script at 'file:///C:/.../learning-react/index.jsx' from origin 'null' has been blocked by CORS policy: Cross origin requests are only supported for protocol schemes: chrome, chrome-extension, chrome-untrusted, data, http, https, isolated-app.
```

- I've found that I need to use a local server tool to serve my app and open the app from browser;<sup>[4](#1-references)</sup>
- Beyond that I've found the official installation process for React projects<sup>[5](#1-references)</sup>: https://react.dev/learn/creating-a-react-app
- Created React project using `React Router` framework;<sup>[6](#1-references)</sup>

```powershell
npx create-react-router@latest
```

> **INFO:** The command opens a prompt with some steps to create the project. I've used the default values and a project folder was create at `./my-react-router-app`.

- With this command discovered about the `npx` and the its difference to `npm` command;<sup>[7](#1-references)</sup>
- I've decided to come back to scrimba, lets work with project later. Probably they will show how to work locally;

### 2.4. First React Challenge

Nothing special here.

### 2.5. Local Setup w/ Vite

- As I've imagined, they show us a way to create/run a React project locally. In this case, they show about Vite;
- Some steps I've already done, let's create the Vite project with:

```powershell
npm create vite@latest
```

- I've followed the wizard instructions and created the `first-vite-project` project;
- Project installed an running by executing:

```powershell
npm install
npm run dev
```

### 2.6. Libraries/Frameworks

- Nothing special here, he just shows the concept about libraries and frameworks, some history of them, etc.

### 2.7. React.createElement()

- The way he showed the root.render function, passing an html statement directly to it, it's kinda a new thing in React. At the begining, the way to create an document element was using `createElement` function from `"react"` lib. 
- This function receives three parameters:
  - The type of element;
  - Props
  - The children of this element;

- This function returns a javascript object like:

```js
{
    type: 'h1',
    key: null,
    props: {
        children: 'Hello from createElement!'
    },
    _owner: null,
    _store: {}
}
```

### 2.8. JSX

- Using the `createElement` for creating nested elements can be very verbose, like for create something like this:

```html
<h1>
    <span>
        "I'm inside the span"
    </span>
</h1>
```
- ...You need to do this:

```js
const reactElement = createElement("h1", null, createElement("span", null, "I'm inside the span"))
```

- With JSX you cand do only this:

```js
const reactElement = <h1><span>"I'm inside the span"</span></h1>
```

### 2.9. Why React? It's Composable!

- Talking about reusability, the narrator showed an example of navigation bar using bootstrap lib. If you need to reuse the bar in several pages (in different .html files) you need to copy-and-paste the bar's code in each one of them.
- Using components you can create a custom html tag (or custom component) and reuse it through your code. The component encapsulates the code you want and you just need use the tag for replicate your piece of code.
- To create a new component you just need to create a fuction called with the name you want to component, and this function must return the JSX element you want in HTML, for example:

```js
function MyComponent() {
    return <h1>Some header</h1>
}

root.render(
    // ...
    <MyComponent />
    // ...
)
```

### 2.10. Why React? It's Declarative!

- It's showed the difference between declarative vs imperative:
  - Declarative: says what is need to be done
  - Imperative: says how it is need to be done

- It gave us a challenge to append an h1 element to root div, using the vanilla JS functions. To do that i used the `document.createElement` function <sup>[8](#1-references)</sup>

```js
const rootElement = document.getElementById("root")
const headerElement = document.createElement("h1")

headerElement.className = "header"
rootElement.appendChild(headerElement)

const headerContent = document.createTextNode("Hello, React!")

headerElement.appendChild(headerContent)
```

- ...Proposed solution:

```js
const h1 = document.createElement("h1")
h1.textContent = "This is imperative coding"
h1.className = "header"
document.getElementById("root").appendChild(h1)
```

- This contranst with the React works, once you just say to the lib what needs to be done, and it renders what you ask:

```js
import { createRoot } from "react-dom/client"
const root = createRoot(document.getElementById("root"))

root.render(
    <h1 className="header">Hello, React!</h1>
)
```

### 2.11. Random housekeeping

- If you change the script tag in .html file to use "index.js" instead of "index.jsx" the code still works. Howerver, once we use Vite under the hood, his document recomment using `.jsx` any time a React-specific syntax is used, for "performance" purposes. Not performance exactly, but Vite will work "smootthly" this way, like the narrator said;
- He talked about some possible problems with image relative paths, specially when running code outside scrimba. He suggests to use absolute paths to image like this:

```js
root.render(
    <img src="/src/assets/react-logo.png" />
)
```
- Another point he showed to housekeeping is about rendering multiple element. When you try to do this:

```js
root.render(
    <img src="/src/assets/react-logo.png" />
    <h1>This is another element</h1>
)

```

- ... It is like the same thing doing this:

```js
import { createElement } from "react"

// ...

createElement()createElement()
```

- ...So to create multiple elements he suggests to put all ement into a unique `<div>` (or any other tag) element, like this:

```js
root.render(
    <div>
        <img src="/src/assets/react-logo.png" />
        <h1>This is another element</h1>
    </div>
)
```
