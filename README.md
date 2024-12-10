# React useEffect Hook Not Re-rendering on Data Change

This repository demonstrates a common issue with the React `useEffect` hook where it fails to trigger re-renders when data changes.  The provided `bug.js` file shows the erroneous code, while `bugSolution.js` presents the solution.

## Problem

A React component fetches data using `fetch`. After the initial data fetch, if the data changes on the server side, the component does not update. This occurs because the `useEffect` hook's dependency array is empty (`[]`), causing it to run only once after the initial render.

## Solution

The solution involves adding the data state variable to the `useEffect` hook's dependency array. This ensures that `useEffect` reruns whenever `data` changes, leading to a re-render of the component with the updated data.

## How to run

1. Clone the repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
