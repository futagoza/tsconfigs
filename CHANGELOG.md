## v4.0.0 _(08/06/2026)_

* Drop support for Node 12-19; Node 20 (and ES2023) is the target version in my projects right now
* Restructure all options (and groups) in `tsconfig.json` to follow order of appearance on `https://www.typescriptlang.org/tsconfig/`
* Update existing options in `tsconfig.json` (e.g. target ES2022) and add new options from TypeScript _v4.3_ to _v6.0_
* `@futagoza/tsconfig/browser` now extends `@futagoza/tsconfig/browser/modern` which now targets _ES2020_
* `@futagoza/tsconfig/browser/evergreen` now targets _ES2025_
* `@futagoza/tsconfig/browser/webworker` now targets _ES2020_
* Remove `@futagoza/tsconfig/node/*.modules` configs; due to switching to _ES2022 modules_ by default, these are now redundant
* `@futagoza/tsconfig/node/lts` (and by extension `@futagoza/tsconfig/node`) now targets _ES2023_
* `@futagoza/tsconfig/node/current` now targets _ES2025_
* Remove _dom.iterable_ and add _decorators_ libs for `@futagoza/tsconfig/dev`
* Updated base `README.md` to account for the recent changes
* DEV: Update the root `$schema` property in each config to use `https` because VS Code now has trust issues with `http`

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
