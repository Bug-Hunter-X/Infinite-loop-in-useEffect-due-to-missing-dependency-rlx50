# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by a missing dependency array in the `useEffect` hook. 

## Bug Description

The `useEffect` hook in `bug.js` is designed to log the current count to the console whenever it changes. However, because the dependency array `[count]` is missing, the effect runs on every render, causing the component to re-render endlessly. This leads to a crash in the browser.

## Solution

The solution, found in `bugSolution.js`, addresses the issue by correctly specifying the dependency array `[count]`. Now, the effect only runs when the value of the `count` state variable changes.