# React Router v6 Catch-All Route Issue

This repository demonstrates a problem with the catch-all route (`/*`) in React Router v6. The catch-all route, intended to handle any unmatched routes, is being unexpectedly ignored.

## Problem Description

In the provided `App.js` file, a catch-all route is added to handle any unmatched paths. However, this route is not working correctly.  If you navigate to a path that doesn't match `/` or `/about`, instead of showing the NotFound component, the browser defaults to the `/` route.

## Solution

The issue arises from the order of routes. The catch all route must be placed as the last route in Routes component.  The solution involves moving the catch-all route to the end of the `Routes` component. This ensures it only matches when no other routes match.