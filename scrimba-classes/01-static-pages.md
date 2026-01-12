# Static pages classes

## 1. References

1. https://stackoverflow.com/a/31520672/26058659
2. https://github.com/coreybutler/nvm-windows
3. https://github.com/coreybutler/nvm-windows/releases
4. https://stackoverflow.com/a/66951910/26058659
5. https://stackoverflow.com/a/56121123/26058659
6. https://react.dev/learn/creating-a-react-app#react-router-v7
7. https://www.freecodecamp.org/news/npm-vs-npx-whats-the-difference/

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

- The way he showed the root.render function, passing an html statement directly to it, it's kinda a ney thing in React. At the begining, the way to create an document element was using `createElement` function from `"react"` lib. 
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
