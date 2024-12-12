# React 19 useEffect Interval Cleanup

This repository demonstrates a common error in React 19 involving the `useEffect` hook and `setInterval`.  Forgetting to clear the interval when the component unmounts can lead to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains code that uses `setInterval` within `useEffect` but fails to provide a cleanup function.  This means the interval continues to run even after the component is unmounted.

## Solution
The `bugSolution.js` file provides the corrected code with a cleanup function that clears the interval using `clearInterval`.