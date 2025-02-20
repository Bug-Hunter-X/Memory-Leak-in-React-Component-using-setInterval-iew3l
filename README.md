# React setInterval Memory Leak
This repository demonstrates a common error in React components: using `setInterval` within `useEffect` without a cleanup function. This leads to a memory leak because the interval continues to run even after the component is unmounted.

The `bug.js` file contains the buggy code. The `bugSolution.js` file shows the corrected code with the necessary cleanup function to avoid the memory leak.

## How to reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console. The `bug.js` component should cause a memory leak (check the browser's developer tools).
5. Switching to `bugSolution.js` will show that the memory leak is fixed.