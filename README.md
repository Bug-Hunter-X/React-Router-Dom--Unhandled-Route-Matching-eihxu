# React Router Dom Unhandled Route Matching
This repository demonstrates an issue with React Router Dom v6 where unexpected behavior occurs when no route matches the current URL.  The issue is that a missing route that handles the catch-all scenario will cause the application to throw an error, instead of rendering a default route.

## How to Reproduce
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to a path that does not have a defined route (e.g., `/nonexistent`).

## Solution
The solution is to add a catch-all route using `Route` with the `path="*"` prop in your `Routes` component.