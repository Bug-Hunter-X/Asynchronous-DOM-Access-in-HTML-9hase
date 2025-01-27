# Asynchronous DOM Access Bug in HTML
This repository demonstrates a common, yet subtle, bug in HTML involving asynchronous access to DOM elements.  The problem arises when JavaScript code attempts to manipulate a DOM element before the browser has finished rendering it. 

## Bug Description
The `bug.html` file contains a `div` element with some text content. A JavaScript script attempts to change the `display` style of this `div` to `none`, making it invisible. However, this attempt happens *before* the browser has fully loaded the DOM. This is an asynchronous process, meaning the script runs before the DOM is ready.

## Solution
The `solution.html` file demonstrates a correct approach, using the `DOMContentLoaded` event listener to ensure the script executes only after the DOM is fully parsed and ready. 