# React Router v6 Nested Route Conflict

This repository demonstrates a common issue with nested routes in React Router v6: route conflicts when using overly broad wildcard routes.

## Bug Description
The bug arises when defining a route like '/about/*'.  This route matches any path that begins with '/about', even '/about' itself.  If a more specific route such as '/about' exists, it will be overshadowed and not rendered correctly. This leads to unexpected rendering and navigation issues.

## Solution
The solution involves carefully considering the route hierarchy and avoiding unnecessary wildcard routes when more specific routes are already in place.  Instead of using '/about/*', it's often better to define nested routes within the '/about' route to handle sub-routes.