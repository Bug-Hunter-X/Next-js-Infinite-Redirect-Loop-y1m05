# Next.js Infinite Redirect Loop Bug

This repository demonstrates a common error in Next.js applications: an infinite redirect loop caused by using the `useRouter` hook to push to the current route.  This can happen when a component attempts to redirect to the same route it is already on, causing it to continuously redirect.

## Bug

The `bug.js` file contains a component with a button that redirects to the root ('/') route. If the user is already on the root route when the button is clicked, this triggers an infinite redirect loop, leading to a poor user experience and potentially browser crashes.

## Solution

The `bugSolution.js` file provides a solution by checking the current route before performing the redirect. This prevents the infinite loop by only redirecting if the current route is different from the target route.