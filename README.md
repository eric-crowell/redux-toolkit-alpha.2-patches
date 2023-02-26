# Redux Toolkit Alpha 2.0 Patches for PNPM Package Manager

Patches `@reduxjs/toolkit@2.0.0-alpha.2` for projects that use Typescript and have their `moduleResolution` configured to `node16` or `nodenext`.

Unblocks projects that need to use `node16` to utilize the `exports` feature.

## How to Use

Copy the `patches` folder to the root of your project. Add the following to `package.json`...

```json
"pnpm": {
  "patchedDependencies": {
    "redux@5.0.0-alpha.2": "patches/redux@5.0.0-alpha.2.patch",
    "redux-thunk@3.0.0-alpha.1": "patches/redux-thunk@3.0.0-alpha.1.patch",
    "@reduxjs/toolkit@2.0.0-alpha.2": "patches/@reduxjs__toolkit@2.0.0-alpha.2.patch",
    "immer@9.0.19": "patches/immer@9.0.19.patch",
    "reselect@4.1.7": "patches/reselect@4.1.7.patch"
  }
}
```

Run `pnpm install` to apply.