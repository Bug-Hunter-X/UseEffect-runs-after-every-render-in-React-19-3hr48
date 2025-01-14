# React 19 useEffect Performance Issue

This repository demonstrates a common performance issue in React 19 related to the `useEffect` hook.  The issue arises when the dependency array is omitted or incorrectly specified, leading to unnecessary re-renders and potential performance degradation.

## Bug Description

The provided code snippet shows a simple counter component. However, because the useEffect hook lacks a dependency array, it runs after every render, logging the count to the console. In larger applications, this can lead to significant performance problems.

## Solution

The solution involves correctly specifying the dependencies for the useEffect hook. By including `count` in the dependency array, the effect only runs when the `count` value changes, fixing the performance issue.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console output and the frequent re-rendering.