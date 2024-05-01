# @vitetw/vite-plugin-twob

> 🚀 A Vite plugin that obfusates Tailwind classes.

- Lightweight
- Works with both SPA, SSG and SSR.
- Works well with Remix and Astro.
- Works well with mixed classes:
  - `even:bg-slate-50 peer-[:nth-of-type(3)_&]:block odd:lg:bg-red-50 even:lg:bg-slate-300`
  - `hidden peer-[.is-dirty]:peer-required:block`

<sub><sup>_Note: This is just a document. I am using this plugin privately._</sup></sub>

## Setup

### `.npmrc`

```sh
@vitetw:registry=https://npm.pkg.github.com
```

```sh
npm install @vitetw/vite-plugin-twob@beta
```

### `vite.config.js`

```mjs
import twobPlugin from '@vitetw/vite-plugin-twob';

export default defineConfig({
  // ...
  plugins: [twobPlugin()],
  // ...
});
```

```yml
{ 'scripts': { 'build': 'twob path/to/you-entrypoint-css.css && npm run your-build-cmd' } }
```

- Astro: `twob node_modules/@astrojs/tailwind/base.css`

```sh
# run build as usual
npm run build
```
