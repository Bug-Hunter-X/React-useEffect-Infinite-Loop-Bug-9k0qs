# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.

## Bug Description
The `MyComponent` component uses `useEffect` to update a counter every second. However, the dependency array is empty (`[]`), meaning the effect runs after every render, leading to an infinite loop.

## Solution
The solution involves adding `count` to the dependency array so that the effect only runs when `count` changes.