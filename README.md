# CSS Specificity Gotcha: Unexpected Style Behavior

This repository demonstrates a subtle but important issue related to CSS specificity.  The code showcases a situation where a seemingly more targeted class selector fails to override a parent's style due to the higher specificity of an ID selector.

## The Problem

In the `bug.css` file, we have a `div` element with a default blue color.  We then attempt to change the color of `div` elements within a class `.special` to red and the color of `div` with the `id` `myDiv` to green.

The unexpected behavior is that the class selector, despite its apparent higher specificity, does not override the base color, while the id selector overrides it successfully. This is due to the lower specificity of class selectors compared to ID selectors.

## The Solution

The `bugSolution.css` file provides a corrected approach. Understanding CSS specificity is crucial to avoid such issues. 

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` (or create a simple HTML file referencing `bug.css`) in your browser.
3. Observe the unexpected styling of the div elements.
4. Now open `bugSolution.html` (or create an HTML file referencing `bugSolution.css`), and note the correct styling.