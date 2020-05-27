# boilerplate that enables pwa functionality in basic svelte template

this boilerplate is designed for enabling PWA (with offline functionality) in basic [Svelte](https://github.com/sveltejs/template) template

## how to use it:

install rollup-plugin-workbox

```bash
npm install --save rollup-plugin-workbox
```

add this lines to the top of rollup.config.js:

```javascript
import { injectManifest } from 'rollup-plugin-workbox';

const workboxConfig = require('./public/workbox-config.js')
```

add this to plugins section in rollup.config.js:

```javascript
injectManifest(workboxConfig)
```
add files from 'public' directory to your project`s 'public' directory (replace 'index.html')

main rules for caching are written in workbox-config.js file
