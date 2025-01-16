# Uncommon HTML DOM Manipulation Bug

This repository demonstrates a subtle bug that can occur when working with the Document Object Model (DOM) in HTML and JavaScript. The bug arises from attempting to access a property of an object that is null, often due to incorrect element selection or timing issues.  The solution highlights best practices for handling such situations.

## Bug Description
The `bug.html` file contains a simple HTML structure. The JavaScript code attempts to access an element using `document.getElementById("myDiv").querySelector("p")`. However, if the element selection fails (e.g., if "myDiv" doesn't exist, or if it doesn't contain a paragraph element), the resulting `element` variable will be null.  Subsequently, attempting to access `element.style.color` will throw a TypeError.

## Solution
The `bugSolution.html` file provides a corrected version. It uses optional chaining (`?.`) to safely access the property, preventing the error. If `element` is null, the expression short-circuits, avoiding the error.  This technique is a clean and modern approach.