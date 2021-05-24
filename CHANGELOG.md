## v3.0.0 _(25/05/2021)_

* Drop support for Node 10 _(Hi Node 12)_
* Update base `tsconfig.json` with options from TypeScript _v4.0_ to _v4.3_ while enabling the following options:
    - `disableFilenameBasedTypeAcquisition`
    - `noImplicitOverride`
    - `noUncheckedIndexedAccess`
* Updated (while also restructuring) current configs
* Added more configs (more configuration profiles for both the browser and node)
* Updated base `README.md`
    - Set requirement for TypeScript to v4.3
    - Updated current config sections
    - Added new config sections

## v2.1.0 _(21/08/2020)_

* Update JSX options _(that are commented, so technically not in use)_
* Enable the `esModuleInterop` and `skipLibCheck` options for a better development experience
* Add ESNext based config at `@futagoza/tsconfig/dev`

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
* Update and restructure base `tsconfig.json` using the [new `tsconfig` reference guide](https://www.typescriptlang.org/tsconfig)
* Target ES2018 now when using `@futagoza/tsconfig/node`
* Target ES2019 now when using `@futagoza/tsconfig/desktop`

## v1.0.0 _(11/07/2019)_

* Initial Release
