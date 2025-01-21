# React Native useEffect Cleanup Issue

This repository demonstrates a common but often overlooked error in React Native: failing to properly clean up asynchronous operations within the `useEffect` hook.  Improper cleanup can lead to memory leaks and unexpected behavior.

## The Problem

The `bug.js` file showcases code that subscribes to a data stream but lacks a cleanup function to unsubscribe when the component unmounts. This results in a persistent subscription even after the component is no longer needed.

## The Solution

The `bugSolution.js` file provides the corrected code.  It includes a cleanup function returned from `useEffect` that unsubscribes from the data stream when the component unmounts, preventing memory leaks.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run the application (instructions may vary depending on your development environment).
4. Observe the behavior in `bug.js` and compare it to the corrected behavior in `bugSolution.js`.