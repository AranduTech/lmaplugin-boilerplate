# lmaplugin-boilerplate

This is a boilerplate for creating a plugin for Laravel Mui Admin.

## Before you start

1. Replace all occurrences of `lmaplugin-boilerplate` with your plugin name, as it will be used as the npm package name.

2. Replace all occurrences of `BoilerplatePlugin` with your plugin class name.

3. Also rename the `src/BoilerplatePlugin.ts` file to your plugin class name.

> Replace EVERY occurrence in the projeect, including the readme, package.json, etc.

## Usage

Install the plugin in your Laravel Mui Admin project

```bash
npm install --save lmaplugin-boilerplate
```

Require the plugin in your `resources/js/plugins.js` file, and add it to exported array

```js
import BoilerplatePlugin from 'lmaplugin-boilerplate';

export default [
  // ...
  BoilerplatePlugin,
];
```

## Development

```bash
# install dependencies
npm install
# build for production
npm run build
```

For real-time development, see the [`link` documentation](docs/link.md) for instructions on linking the plugin to a consumer project.

