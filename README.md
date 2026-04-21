# @guoyunhe/tsconfig

[![npm version](https://img.shields.io/npm/v/@guoyunhe/tsconfig)](https://www.npmjs.com/package/@guoyunhe/tsconfig)
[![npm downloads](https://img.shields.io/npm/dm/@guoyunhe/tsconfig)](https://www.npmjs.com/package/@guoyunhe/tsconfig)

TypeScript configuration presets.

## Node.js ESM

A modern TypeScript configuration for Node.js projects using ES modules (ESM).

### Install

```sh
npm install --save-dev @guoyunhe/tsconfig
```

### Usage

`tsconfig.json`:

```json
{
  "extends": "@guoyunhe/tsconfig/node-esm.json",
  "compilerOptions": {
    "outDir": "dist",
    "rootDir": "src"
  }
}
```

`package.json`:

```json
{
  "type": "module"
}
```

### Options

| Option              | Value        | Description                                                     |
| ------------------- | ------------ | --------------------------------------------------------------- |
| `lib`               | `["ES2022"]` | Includes ES2022 built-in APIs                                   |
| `module`            | `NodeNext`   | Uses Node.js native ESM resolution with `.js` extension imports |
| `moduleResolution`  | `NodeNext`   | Resolves modules using Node.js ESM algorithm                    |
| `target`            | `ES2022`     | Compiles to ES2022 JavaScript                                   |
| `strict`            | `true`       | Enables all strict type-checking options                        |
| `esModuleInterop`   | `true`       | Allows default imports from CommonJS modules                    |
| `skipLibCheck`      | `true`       | Skips type checking of declaration files                        |
| `declaration`       | `true`       | Generates `.d.ts` declaration files                             |
| `allowImportingTsExtensions` | `true` | Allows imports with `.ts` extensions                      |

## React

A modern TypeScript configuration for React projects using ES modules (ESM) and a bundler like Vite or webpack.

### Install

```sh
npm install --save-dev @guoyunhe/tsconfig
```

### Usage

`tsconfig.json`:

```json
{
  "extends": "@guoyunhe/tsconfig/react.json",
  "compilerOptions": {
    "baseUrl": "src"
  },
  "include": ["src"]
}
```

### Options

| Option              | Value                          | Description                                                     |
| ------------------- | ------------------------------ | --------------------------------------------------------------- |
| `lib`               | `["ES2022", "DOM", "DOM.Iterable"]` | Includes ES2022 and browser built-in APIs                  |
| `module`            | `ESNext`                       | Uses ESNext module format for bundlers                          |
| `moduleResolution`  | `Bundler`                      | Resolves modules using bundler algorithm (Vite, webpack, etc.)  |
| `target`            | `ES2022`                       | Compiles to ES2022 JavaScript                                   |
| `jsx`               | `react-jsx`                    | Uses React 17+ automatic JSX transform                          |
| `strict`            | `true`                         | Enables all strict type-checking options                        |
| `esModuleInterop`   | `true`                         | Allows default imports from CommonJS modules                    |
| `skipLibCheck`      | `true`                         | Skips type checking of declaration files                        |
| `allowImportingTsExtensions` | `true`              | Allows imports with `.ts` and `.tsx` extensions                 |
| `noEmit`            | `true`                         | Does not emit output files (bundler handles emission)           |

## License

MPL-2.0
