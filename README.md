## Steps to reproduce

1. `npm install`
2. `node index.js`

## Expected behaviour

Workbox-build does not look for babel.config.js up the directory tree.

## Actual behaviour

Workbox-build looks for babel.config.js. This causes an error if the resolved config contains @babel/plugin-transform-runtime:

```
Error: Unable to write the service worker file. 'Runtime helpers are not enabled. Either exclude the transform-runtime Babel plugin or pass the `runtimeHelpers: true` option. See https://github.com/rollup/rollup-plugin-babel#configuring-babel for more information
```
