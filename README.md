# Learning React

> Repo created to help in my React study.

## 1. Context

Currently i am searching for new jobs and I am needing to studying some stuff to get updated. Beyond that, I've have software company in my name and I want to search new projects.
So I've decide to create a website for company / a personal web portfolio using React, because I've already know some stuff about Javascript/Typescript, and a little less about HTML/CSS. Currently I work with C and Python, but I've loved the typing system in Typescript. So, let's go with React hehe

## 2. References

1. https://stackoverflow.com/a/31520672/26058659
2. https://github.com/coreybutler/nvm-windows
3. https://github.com/coreybutler/nvm-windows/releases

## 3. scrimba.com

To study React I've received some suggestion to follow this tutorial: https://scrimba.com/learn-react-c0e

## 4. Personal Notes

I am using the repo to train english also, witn no judgment, no concern about mistakes, only write. Maybe somehting like a diary, i dont know. But to put this in practice.
I like the ide to use Markdown to keep my notes, it's simple and beautiful. And somehow I imagine me like a wizard in Harry Potter taking some notes about a new spell. Anyway, I am tripping a little XD...

### 4.1. Static pages

#### 4.1.1. Course Introduction

- The comparison between playing an instrument and to program is so real. I have a "problem" that I wanna to learn any tech tool/language at same time I wanna to put in the "best" way. I love clean code, to organize/refactor my projects, but this is stucking some how....So I liked the idea of this kind of tutorial, and I need to practice, to learn, forgettin about optimizing, best patterns, etc...


#### 4.1.2. What we'll learn

- Nothing special here, just they showing the course content.

#### 4.1.3 First React Code

> **INFO** I am using Windows to run this project, so any command, process showed below is relative to this OS.

- Amazing! The "video" shares the same editor with me. How do they do that? 
- Instead of writing the code on Scrimba, I will try to replicate their code here in VSCode.
- First, I am installing the `react` and `react-dom` dependencies via `npm`;
  - Updated my local `npm` version by running:<sup>[1](#2-references)</sup>

```powershell
npm install -g npm
```

  - Installed the `nvm-windows` tool. This tool helps manage multiple installations of node.js.<sup>[2,3](#2-references)</sup>
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
