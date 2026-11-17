# Decimal to Binary Converter

![freeCodeCamp logo](https://design-style-guide.freecodecamp.org/downloads/fcc_secondary_large.svg)

A small web application that converts decimal numbers into binary numbers. It was created as part of the freeCodeCamp JavaScript Algorithms and Data Structures curriculum while learning recursion.

> **Learning note:** This was not my favorite project in the curriculum. However, I decided it was worth including because understanding binary numbers is an important foundation for developers. Binary is used throughout computing, including data representation, bitwise operations, memory, networking, and computer architecture.

## What It Does

- Accepts a non-negative decimal number.
- Converts the number to binary using a recursive `decimalToBinary()` function.
- Supports conversion with the **Convert** button or the **Enter** key.
- Displays an educational call-stack animation when converting the number `5`.
- Rejects empty, invalid, and negative input values.

## Technologies

- HTML5
- CSS3
- JavaScript

## How Recursion Is Used

The converter repeatedly divides the input by `2` until it reaches the base case of `0` or `1`. As each recursive call returns, the remainder from each division is added to the result:

```js
const decimalToBinary = (input) => {
  if (input === 0 || input === 1) {
    return String(input);
  }

  return decimalToBinary(Math.floor(input / 2)) + (input % 2);
};
```

The special animation for `5` makes the recursive call stack visible:

```text
decimalToBinary(5)
  -> decimalToBinary(2)
    -> decimalToBinary(1)
```

## Running the Project

1. Clone or download this repository.
2. Open `index.html` in a web browser.
3. Enter a non-negative decimal number.
4. Select **Convert** or press **Enter**.

No build tools or dependencies are required.

## Project Files

| File | Purpose |
| --- | --- |
| `index.html` | Defines the converter interface and output areas |
| `styles.css` | Provides the layout, colors, responsive design, and animation styling |
| `script.js` | Handles validation, conversion, recursion, and the call-stack animation |

## Learning Takeaways

This project reinforced:

- How recursive functions use a base case to stop execution.
- How the call stack stores and resolves nested function calls.
- How decimal values can be converted into binary using division and remainders.
- How JavaScript can update a page dynamically through the DOM.
- How input validation protects the user experience.

## Attribution

This project was completed as part of the [freeCodeCamp JavaScript Algorithms and Data Structures curriculum](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures-v8/learn-recursion-by-building-a-decimal-to-binary-converter/).

The curriculum and project concept belong to [freeCodeCamp](https://www.freecodecamp.org/). This repository documents my completed learning exercise and implementation.
