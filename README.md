> This package contains configuration files for TypeScript v4.3+<br>
> Require's [tslib](https://www.npmjs.com/package/tslib) as a dependency for outputted code.

A collection of configuration files I use with _[tsconfig.json](https://www.typescriptlang.org/tsconfig)_ while working with TypeScript.

## installation

```console
$ npm i --save-dev @futagoza/tsconfig
$ npm i tslib
```

## usage

Put the following into your `tsconfig.json` (__hint:__ you can rename this file when using `tsc -p "custom name"`):

```json
{
    "extends": "@futagoza/tsconfig"
}
```

## configurations

#### `@futagoza/tsconfig` _(or `@futagoza/tsconfig/tsconfig.json`)_

- Target ES2015
- Use CommonJS module generator
- Strict type checking
- Resolve JSON files
- Enables source maps (with the original source included in the source maps)
- Declaration files
- Always use Unix style (`lf`) new lines
- Do not emit on errors
- Always import helpers from tslib to avoid duplication of TypeScript helpers
- Exclude's a number of directories that shouldn't contain `*.ts` source files
- Includes commonly used directories for `*.ts` source files
- Disable's automatic type acquisition
- Allows importing `*.js` exports into `*.ts` files
- Enforces consistent casing in filenames (when importing)
- Does not emit declarations for code that has an `@internal` annotation
- Enable and disable options for my most common use cases

#### `@futagoza/tsconfig/browser.json` _(or `@futagoza/tsconfig/browser/legacy.json`)_

- Extends `@futagoza/tsconfig`
- Target ES5
- Generate UMD modules

#### `@futagoza/tsconfig/browser/evergreen.json`

- Extends `@futagoza/tsconfig`
- Target ES2020
- Generate ES2020 modules _(ES2015 modules + dynamic imports + `import.meta` support)_

#### `@futagoza/tsconfig/browser/modern.json`

- Extends `@futagoza/tsconfig`
- Target ES2018
- Generate ES2015 modules

#### `@futagoza/tsconfig/webworker.json`

- Extends `@futagoza/tsconfig`
- Target ES2015
- Use _no_ module generator

#### `@futagoza/tsconfig/node/core.json`

- Extends `@futagoza/tsconfig`
- Enables the `skipLibCheck` option
- The `@types/node` type package is included without being referenced

#### `@futagoza/tsconfig/node.json` _(or `@futagoza/tsconfig/node/lts.json`)_

- Extends `@futagoza/tsconfig/node/core.json`
- Target ES2019 (used in Node.js 12)

#### `@futagoza/tsconfig/node/lts.modules.json`

- Extends `@futagoza/tsconfig/node/lts.json`
- Generate ES2015 modules

#### `@futagoza/tsconfig/node/current.json`

- Extends `@futagoza/tsconfig/node/core.json`
- Target ES2020 (used in Node.js 16)

#### `@futagoza/tsconfig/node/current.modules.json`

- Extends `@futagoza/tsconfig/node/current.json`
- Generate ES2020 modules _(ES2015 modules + dynamic imports + `import.meta` support)_

#### `@futagoza/tsconfig/desktop.json`

- Meant for use with NW.js or Electron
- Extends `@futagoza/tsconfig/browser/evergreen.json`
- The `@types/node` type package is included without being referenced

#### `@futagoza/tsconfig/dev.json`

- Extends `@futagoza/tsconfig`
- Target ESNext _(with library support for browsers, node and web-workers)_
- Use ES module generator

## license

Copyright © 2019+ Futago-za Ryuu<br>
Released under the MIT License, [http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT)
