<p align="center">
  <img src="https://raw.githubusercontent.com/freeCodeCamp/assets/master/assets/logos/Free%20Code%20Camp%20logo.svg" alt="freeCodeCamp logo" width="360">
</p>

<h1 align="center">Decimal to Binary Converter</h1>

<p align="center">
  A small interactive project that turns decimal numbers into binary—and makes recursion visible.
</p>

<p align="center">
  <a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures-v8/learn-recursion-by-building-a-decimal-to-binary-converter/">
    <img src="https://img.shields.io/badge/freeCodeCamp-Learning%20Project-0a0a23?logo=freecodecamp" alt="freeCodeCamp learning project">
  </a>
  <img src="https://img.shields.io/badge/HTML-CSS-JavaScript-1b1b32" alt="Built with HTML, CSS, and JavaScript">
</p>

## About

This browser-based converter was built while learning recursion through freeCodeCamp. Enter a non-negative whole number to see its binary representation. Convert **5** to watch the app animate how recursive calls move through the call stack.

## Features

- Converts non-negative decimal integers to binary.
- Accepts input through the **Convert** button or **Enter** key.
- Animates the recursive call stack for the value `5`.
- Shows a helpful message when the input is empty or negative.
- Runs directly in a browser with no dependencies or build step.

## Recursion, step by step

The function keeps dividing the number by two until it reaches `0` or `1`. As the calls return, it adds each remainder to the result:

```text
decimalToBinary(5)
  -> decimalToBinary(2)
    -> decimalToBinary(1)  // base case
    <- "1"
  <- "10"
<- "101"
```

That process is implemented in JavaScript:

```js
const decimalToBinary = (input) => {
  if (input === 0 || input === 1) {
    return String(input);
  }

  return decimalToBinary(Math.floor(input / 2)) + (input % 2);
};
```

## Run it locally

1. Clone or download this repository.
2. Open `index.html` in a browser.
3. Enter a non-negative whole number and select **Convert** or press **Enter**.

## Built with

HTML, CSS, and vanilla JavaScript.

## Project files

| File | Purpose |
| --- | --- |
| `index.html` | Converter form and output areas |
| `styles.css` | Dark theme, responsive layout, and call-stack animation styles |
| `script.js` | Input handling, recursive conversion, and animation |

## Learning project credit

Created as part of freeCodeCamp's [Learn Recursion by Building a Decimal to Binary Converter](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures-v8/learn-recursion-by-building-a-decimal-to-binary-converter/) curriculum.

The curriculum and freeCodeCamp logo belong to [freeCodeCamp](https://www.freecodecamp.org/). This repository is my implementation of the learning project.
