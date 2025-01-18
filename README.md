# Uncommon HTML Bug: Incorrect Element Hiding

This repository demonstrates a subtle bug related to hiding an HTML element using JavaScript.  The issue arises from attempting to manipulate the element's display or visibility properties before the element has fully loaded into the DOM.

## The Problem

The `bug.html` file contains a `div` element that should initially be hidden. However, the JavaScript code attempts to hide it before the browser has completed rendering the element. This results in the element remaining visible, despite the JavaScript code seemingly correctly setting the `display` and `visibility` properties.

## The Solution

The solution (`bugSolution.html`) addresses this issue by ensuring the JavaScript code executes only after the DOM is fully loaded.  This is achieved by placing the JavaScript code within a `DOMContentLoaded` event listener. This ensures that the element exists before attempting to hide it.