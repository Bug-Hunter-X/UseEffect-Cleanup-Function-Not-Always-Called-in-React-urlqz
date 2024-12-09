# useEffect Cleanup Function Not Always Called in React

This repository demonstrates a common issue with the `useEffect` hook in React functional components: the cleanup function not being called as expected.

## Problem
The example code includes a `useEffect` hook with a cleanup function. Ideally, this function should run before the component unmounts or before the next render, allowing for resource cleanup (e.g., clearing timers, event listeners, etc.). However, due to a missing dependency in the useEffect dependency array the cleanup function may not always be called. This results in unexpected behavior or potential memory leaks.

## Solution
The solution involves correctly specifying dependencies in the `useEffect` dependency array. By including `count` in the dependency array, the effect will run after every render and the cleanup function will be called appropriately. 