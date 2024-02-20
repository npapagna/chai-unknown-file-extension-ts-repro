#  Unknown file extension ".ts" Chai bug repro

## Description

This repository contains a minimal example to reproduce the following error.
It happens when using `chai` `5.0.0` or later.

```text
TypeError: Unknown file extension ".ts" for /Users/nicopm/WebstormProjects/chai-unknown-file-extension-ts-repro/test/repro.ts
    at Object.getFileProtocolModuleFormat [as file:] (node:internal/modules/esm/get_format:160:9)
    at defaultGetFormat (node:internal/modules/esm/get_format:203:36)
    at defaultLoad (node:internal/modules/esm/load:141:22)
    at async ModuleLoader.load (node:internal/modules/esm/loader:409:7)
    at async ModuleLoader.moduleProvider (node:internal/modules/esm/loader:291:45)
    at async link (node:internal/modules/esm/module_job:76:21)
```

## Steps to reproduce

1. Install [nvm](https://github.com/nvm-sh/nvm)
2. Run `nvm install`
3. Run `npm install`
4. Run `npm test`
5. Notice the command fails with the error message provided above.
6. Change the `chai` version to `4.4.1`.
7. Run `npm test`
8. Notice the test run fine now.

