# Learning React

> Repo created to help in my React study.

## 1. Context

Currently i am searching for new jobs and I am needing to studying some stuff to get updated. Beyond that, I've have software company in my name and I want to search new projects.
So I've decide to create a website for company / a personal web portfolio using React, because I've already know some stuff about Javascript/Typescript, and a little less about HTML/CSS. Currently I work with C and Python, but I've loved the typing system in Typescript. So, let's go with React hehe

## 2. References

1. https://stackoverflow.com/a/31520672/26058659
2. https://github.com/coreybutler/nvm-windows
3. https://github.com/coreybutler/nvm-windows/releases
4. https://stackoverflow.com/a/66951910/26058659
5. https://stackoverflow.com/a/56121123/26058659
6. https://react.dev/learn/creating-a-react-app#react-router-v7
7. https://www.freecodecamp.org/news/npm-vs-npx-whats-the-difference/

## 3. scrimba.com

To study React I've received some suggestion to follow this tutorial: https://scrimba.com/learn-react-c0e

## 4. Personal Notes

I am using the repo to train english also, witn no judgment, no concern about mistakes, only write. Maybe somehting like a diary, i dont know. But to put this in practice.
I like the ide to use Markdown to keep my notes, it's simple and beautiful. And somehow I imagine me like a wizard in Harry Potter taking some notes about a new spell. Anyway, I am tripping a little XD...

### 4.1. Static pages

#### 4.1.1. Course Introduction

- The comparison between playing an instrument and to program is so real. I have a "problem" that I wanna to learn any tech tool/language at same time I wanna to put in the "best" way. I love clean code, to organize/refactor my projects, but this is stucking some how....So I liked the idea of this kind of tutorial, and I need to practice, to learn, forgettin about optimizing, best patterns, etc...


#### 4.1.2. What we'll learn

Nothing special here, just they showing the course content.

#### 4.1.3 First React Code

> **INFO** I am using Windows to run this project, so any command, process showed below is relative to this OS.

- Amazing! The "video" shares the same editor with me. How do they do that? 
- Instead of writing the code on Scrimba, I will try to replicate their code here in VSCode;
- First, I am installing the `react` and `react-dom` dependencies via `npm`;
- Updated my local `npm` version by running:<sup>[1](#2-references)</sup>

```powershell
npm install -g npm
```

- Installed the `nvm-windows` tool. This tool helps manage multiple installations of node.js;<sup>[2,3](#2-references)</sup>
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

- I've found that I need to use a local server tool to serve my app and open the app from browser;<sup>[4](#2-references)</sup>
- Beyond that I've found the official installation process for React projects<sup>[5](#2-references)</sup>: https://react.dev/learn/creating-a-react-app
- Created React project using `React Router` framework;<sup>[6](#2-references)</sup>

```powershell
npx create-react-router@latest
```

> **INFO:** The command opens a prompt with some steps to create the project. I've used the default values and a project folder was create at `./my-react-router-app`.

- With this command discovered about the `npx` and the its difference to `npm` command;<sup>[7](#2-references)</sup>
- I've decided to come back to scrimba, lets work with project later. Probably they will show how to work locally;

