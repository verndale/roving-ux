# Roving Index

<p style="text-align='center'">
  <img src="https://img.shields.io/npm/dt/@verndale/roving-index.svg" alt="Total Downloads">
  <img src="https://img.shields.io/npm/v/@verndale/roving-index.svg" alt="Latest Release">
  <img src="https://img.shields.io/npm/l/@verndale/roving-index.svg" alt="License">
</p>

> Turns tedious tab UX into a controlled and stateful experience

<br>

###### Features & Why

1️⃣ User's shouldn't need to tab through each item in a list to see the next list  
2️⃣ Providing keyboard list UX should be easy  
3️⃣ Maintaining the last focused element should be easy

<br>

###### Getting Started

### Installation

```bash
npm i @verndale/roving
```

Use the JSDelivr CDN https://cdn.jsdelivr.net/npm/@verndale/roving-index

<br>

### Importing

```js
// import from CDN
import { rovingIndex } from "https://cdn.jsdelivr.net/npm/@verndale/roving-index"; // cdn es2020

// import from NPM
import { rovingIndex } from "@verndale/roving-index"; // npm es6/common modules
const rovingIndex = require("@verndale/roving-index"); // commonjs
```

<br>

###### Syntax

### Quick API Overview

```js
rovingIndex({
  element: node, // required: the container to get roving index ux
  target: "#foo", // optional: a query selector for which children should be focusable
  callback: (el) => el, // optional: callback that receives the focused element
});
```

### Example Usage

```js
import { rovingIndex } from "@verndale/roving-index";

// just one roving ux container
// roving-index will use direct children as focus targets
rovingIndex({
  element: document.querySelector("#carousel"),
});
```

```js
import { rovingIndex } from "@verndale/roving-index";

// many roving ux containers
// passes a custom query selector so the proper elements get focus
document.querySelectorAll(".horizontal-media").forEach((scroller) => {
  rovingIndex({
    element: scroller,
    target: "a",
  });
});
```
