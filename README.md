# Uncommon HTML Bug: Premature innerHTML Modification

This repository demonstrates a subtle bug related to using `innerHTML` in JavaScript before the target HTML element exists in the DOM.  The bug occurs when attempting to modify the `innerHTML` of an element that hasn't been fully loaded yet by the browser.

## Bug Description

The bug is in `bug.html`. The JavaScript tries to change the `innerHTML` of a `div` before the `div` is fully rendered. This results in a runtime error because `document.getElementById` returns null. 

## Solution

The `bugSolution.html` file demonstrates the solution, which involves ensuring the script runs after the DOM is fully loaded (using the `DOMContentLoaded` event listener).
