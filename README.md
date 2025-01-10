# React Native useRef Hook Timing Bug

This repository demonstrates a subtle bug related to the `useRef` hook in React Native.  The issue arises when a component unmounts before a callback function referencing the ref is executed, resulting in an error. This is an infrequent, timing-dependent issue that can be hard to track down.  The solution involves using cleanup functions within the `useEffect` hook to handle potential unmounting situations.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` or `yarn install` to install dependencies.
3. Run the app.  Navigate between screens rapidly to try to trigger the error.  You might need to try a few times.

## Solution

The provided solution uses a cleanup function within the useEffect hook to safely remove the reference in case of unmounting.

## License

MIT