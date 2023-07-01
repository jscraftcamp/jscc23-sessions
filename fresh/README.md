# Fresh
_session by crowlKats (Leo)_

fresh.deno.dev

Only works with Deno, not Node

Setup: copy from webpage
```
deno run -A -r https://fresh.deno.dev jscraftcamp
```

Split up into "islands" and "routes".

Routes is NextJS style file based routing with handlers for handling server side stuff.

Islands hydrate state on the client to achieve interactivity.

You can check the `IS_BROWSER` whether it's server side rendered or in the browser.

Fresh is a frontend and a backend framework. The routes provide handlers and call a `render` function to render the response.

There is a `RouteConfig` to be able to handle special cases of the file based routing.

There is NO build step.

Uses `hyper` under the hood for the Rust http server. No HTTP/3 yet.

Custom handlers for error pages (_404.tsx).

They use twind (smaller / faster alternative to Tailwind)

Plugins allow you to hook into the render pipeline, so changing generation of CSS or JS.

Better workflow, more UI libraries, node compatibility is coming very soon (probably next week?).

`deno fmt` is based on `dprint` (formatter like prettier written in Rust). It's a lot faster than prettier. TypeScript is now using it.

