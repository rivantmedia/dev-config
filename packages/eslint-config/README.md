# How to setup our eslint plugin

## Prerequisites:

- NodeJS & NPM Installation
- A package.json file in your project using the `npm init`, `pnpm init` or `yarn init` commands depending on the package manager.

## Installation using NPM

To install the eslint plugin for [@rivantmedia](https://github.com/rivantmedia), run the following command

```bash
$ npm i @rivantmedia/eslint-config
```

In package.json add this line:

```
"eslintConfig": {
    "extends": "./node_modules/@rivantmedia/eslint.config.mjs"
  },
```

Next.js has built-in support for ESLint. To run ESLint as part of your Next.js build process, add a script to your package.json:

```
{
  "scripts": {
    "lint": "eslint --config ./package.json"
  }
}
```

## Installation using PNPM

To install the eslint plugin for [@rivantmedia](https://github.com/rivantmedia), run the following command

```bash
$ pnpm add @rivantmedia/eslint-config
```

In package.json add this line:

```
"eslintConfig": {
    "extends": "./node_modules/@rivantmedia/eslint.config.mjs"
  },
```

Next.js has built-in support for ESLint. To run ESLint as part of your Next.js build process, add a script to your package.json:

```
{
  "scripts": {
    "lint": "eslint --config ./package.json"
  }
}
```

## Installation using YARN

To install the eslint plugin for [@rivantmedia](https://github.com/rivantmedia), run the following command

```bash
$ yarn add @rivantmedia/eslint-config
```

In package.json add this line:

```
"eslintConfig": {
    "extends": "./node_modules/@rivantmedia/eslint.config.mjs"
  },
```

Next.js has built-in support for ESLint. To run ESLint as part of your Next.js build process, add a script to your package.json:

```
{
  "scripts": {
    "lint": "eslint --config ./package.json"
  }
}
```
