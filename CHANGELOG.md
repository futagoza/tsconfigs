## v2.0.0 _(10/06/2020)_

* Drop support for Node 8 _(Hi Node 10)_
* Update `exclude` option to exclude more directories
* Update `include` option to include more files
* Explicitly disable automatic type acquisition via the `typeAcquisition` option
* Enable `allowJs` option to allow importing `*.js` exports into `*.ts` files
* Explicitly disable the `incremental` option
* Enable `inlineSources` option to allow including the source of `*.ts` files into generated source-maps
* Enable the `experimentalDecorators` option :)
* Explicitly disable the `assumeChangesOnlyAffectDirectDependencies` option
* Enable the `forceConsistentCasingInFileNames` option
* Disable the `suppressImplicitAnyIndexErrors` option (default value)
* Fix some defaults specified in comments
* Update and restructure base `tsconfig.json` in accordance to the [v2 docs](https://www.typescriptlang.org/v2/en/tsconfig)
* Target ES2018 now when using `@futagoza/tsconfig/node`
* Target ES2019 now when using `@futagoza/tsconfig/desktop`

## v1.0.0 _(11/07/2019)_

* Initial Release
