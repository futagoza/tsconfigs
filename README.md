> This package contains configuration files for TypeScript v3.9+<br>
> Require's [tslib](https://www.npmjs.com/package/tslib) as a dependency for outputted code.

A collection of configuration files I use with _[tsconfig.json](https://www.typescriptlang.org/v2/en/tsconfig)_ while working with TypeScript.

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
- Enables source maps (with the original source included in the source maps)
- Declaration files
- Always use Unix style (`lf`) new lines
- Do not emit on errors
- Always import helpers from tslib to avoid duplication of TypeScript helpers
- Exclude's a number of directories that shouldn't contain `*.ts` source files
- Includes commonly used directories for `*.ts` source files
- Disable's automatic type acquisition
- Allows importing `*.js` exports into `*.ts` files
- Disables the `composite` option
- Enables the `noFallthroughCasesInSwitch` option
- Enables the `experimentalDecorators` option
- Disables the `assumeChangesOnlyAffectDirectDependencies` option
- Enforces consistent casing in filenames (when importing)
- Does not emit declarations for code that has an `@internal` annotation
- Enables the `esModuleInterop` option

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
- Target ES2018
- Use CommonJS module generator (inherited from `@futagoza/tsconfig`)
- Enables the `skipLibCheck` option

#### __`@futagoza/tsconfig/desktop`__

- Extends `@futagoza/tsconfig`
- Target ES2019
- Use UMD module generator

#### __`@futagoza/tsconfig/dev`__

- Extends `@futagoza/tsconfig`
- Target ESNext _(with library support for browsers, node and web-workers)_
- Use ES module generator

## license

Copyright © 2019+ Futago-za Ryuu<br>
Released under the MIT License, [http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT)
