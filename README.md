> This package contains configuration files for TypeScript v3+<br>
> Require's [tslib](https://www.npmjs.com/package/tslib) as a dependency for outputted code.

A collection of configuration files I use when working with TypeScript and targeting different JavaScript environments.

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

#### __`@futagoza/tsconfig`__ (or __`@futagoza/tsconfig/tsconfig`__)

- Target ES2015
- Use CommonJS module generator
- Strict type checking
- Resolve JSON files
- Source maps for Emitted files
- Declaration files
- Source maps for Declaration files
- Always use Unix style (`lf`) new lines
- Do not emit on errors
- Always import helpers from tslib to avoid duplication of TypeScript helpers

#### __`@futagoza/tsconfig/browser`__

- Extends `@futagoza/tsconfig`
- Target ES5
- Use UMD module generator

#### __`@futagoza/tsconfig/webworker`__

- Extends `@futagoza/tsconfig`
- Target ES2015
- Use _no_ module generator

#### __`@futagoza/tsconfig/node`__

- Extends `@futagoza/tsconfig`
- Target ES2017

#### __`@futagoza/tsconfig/desktop`__

- Extends `@futagoza/tsconfig`
- Target ES2018
- Use UMD module generator

## license

Copyright © 2019+ Futago-za Ryuu<br>
Released under the MIT License, [http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT)
