# React useEffect Hook Runs Unnecessarily

This repository demonstrates a common issue in React applications where the `useEffect` hook runs even when the dependencies array is empty, leading to unexpected behavior and performance problems. The example showcases a simple counter component, and the solution explains how to prevent the effect from running unnecessarily.

## Problem

The `useEffect` hook in the `bug.js` file is intended to log the current count to the console whenever it changes. However, it logs even during the initial render, when there's no actual change in count because of empty array `[]`.

## Solution

The `bugSolution.js` file shows how to correctly use the `useEffect` hook with a dependency array.  It also demonstrates how to prevent unnecessary renders by introducing a useRef hook to keep track of the component's mounted state to check for unmounted component before accessing the state.This ensures the effect only runs when the count actually changes.
