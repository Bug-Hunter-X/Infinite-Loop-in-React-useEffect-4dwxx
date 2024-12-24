# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: causing an infinite loop by incorrectly updating state within the effect itself.

## Bug Description
The `MyComponent` function uses `useEffect` to increment the `count` state variable. However, the update logic is flawed because it directly sets the state within `useEffect`, causing the effect to run continuously and the component to re-render repeatedly.

## Solution
The solution is to use the functional update form with `setCount` to make sure `useEffect` does not run again infinitely.