# React Router Dom v6 Catch All Route Issue

This repository demonstrates a problem with the catch-all route (`/*`) in React Router DOM v6.  The catch-all route is intended to handle any unmatched routes, but in this case, it's always triggered, even when valid routes exist.

## Problem

The `/*` route in `App.js` should only match when no other routes match. However, it always matches, regardless of the URL.

## Solution

The solution is to ensure the catch all route is placed at the end of the route list after all other routes.  This ensures that other routes will have precedence and the catch-all route is only used when no other route matches.