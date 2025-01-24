# Uncommon React useEffect Bug: Infinite Loop

This repository demonstrates a subtle bug that can occur when using the `useEffect` hook in React without specifying a dependency array.  The bug leads to an infinite rendering loop, significantly impacting performance. 

## The Bug
The `bug.js` file contains the buggy code. The `useEffect` hook is used without a dependency array (`[]`).  This means the effect runs after every render, causing a continuous update cycle as the `count` value changes.  Each update triggers the effect again, leading to the infinite loop. 

## The Solution
The `bugSolution.js` file provides the corrected code. The `useEffect` hook now includes an empty dependency array `[]`.  This ensures that the effect only runs once after the initial render, resolving the infinite loop problem. 

## How to reproduce
1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Observe the behavior in both versions. Note the difference in the console output and the rendering behavior. 

## Key Learning
This example highlights the importance of correctly specifying the dependency array in `useEffect` to prevent unintended re-renders and performance issues. Always consider the dependencies that your effect should react to and include them in the array.