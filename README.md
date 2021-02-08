# TS Code Katas

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a>

> This is part of Academy's [technical curriculum for **The Mark**](https://github.com/WeAreAcademy/curriculum-mark). All parts of that curriculum, including this project, are licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>.

You're now going to reinforce the TDD process and your TypeScript skills by completing a series of Exercism katas.

## Learning Outcomes

- Use a test-driven development process
- Add TypeScript to a JavaScript codebase

## Exercise 1: Exercism Hello World - TypeScript

> 🎯 **Success criterion:** A TypeScript version of the JS 'Hello World' kata

[Exercism](https://exercism.io/) has lots of exercises for a variety of challenges.

Surprisingly (and unfortunately for our desired goals), the TypeScript katas are _not_ a direct translation of the JavaScript katas - for example, the TypeScript Hello World kata uses object-oriented programming, whereas the JavaScript Hello World kata does not.

The goal right now is _not_ to practice or learn object-oriented programming (which can be done in either JavaScript _or_ TypeScript) - it is important not to confuse "this is an object-oriented thing" with "this is a TypeScript thing" - so, instead, we'll convert a JavaScript kata to a TypeScript one manually.

In this exercise, you'll convert the basic JavaScript Hello World challenge into TypeScript.

For now, we'll do this in the same directory where your JS version is, so the TS and JS versions live side-by-side, although you could do this on a copy of your JS directory.

### Installing TypeScript

We're going to install TypeScript our project under `devDependencies` by running:

```bash
yarn add -D typescript
# or, equivalently,
# yarn add --dev typescript
```

### Configuring TypeScript and Jest/Babel

We want to configure TypeScript to have maximum strictness.

This repo includes a `tsconfig.json` which you can just copy and paste into the root of your project.

Because of the way Exercism has set up this project, you'll also need to follow this Jest guide: [Using TypeScript](https://jestjs.io/docs/en/getting-started#using-typescript).

Afterwards, your `babel.config.js` should look like:

```js
module.exports = {
  presets: [
    [
      "@babel/env",
      {
        targets: {
          node: "current",
        },
        useBuiltIns: false,
      },
    ],
    "@babel/preset-typescript",
  ],
};
```

### Converting to TypeScript

Now, it's pretty simple to convert to TypeScript: duplicate the files `hello-world.js` and `hello-world.spec.js`, but turn the `.js` extension into `.ts` - and, when you run the tests, you should see both `hello-world.spec.js` _and_ `hello-world.spec.ts` _both_ passing.

In this case, we haven't _had_ to add in any typings, but we could have:

```ts
// hello-world.ts

export const hello = (): string => {
  return "Hello, World!";
};
```

### Adding type-checking

The Jest docs warn us about the following:

> there are some caveats to using TypeScript with Babel. Because TypeScript support in Babel is purely transpilation, Jest will not type-check your tests as they are run. If you want that, you can use `ts-jest` instead, or just run the TypeScript compiler `tsc` separately (or as part of your build process).

We'll use `tsc` as it is easiest to plugin.

We recommend editing your `test` script in `package.json` as follows:

```json
"test": "yarn test:types && yarn test:spec",
"test:spec": "jest --no-cache ./*",
"test:types": "tsc --noEmit",
```

so that:

1. `yarn test` checks your types before running the test files
2. `yarn test:spec` lets you run test files without checking types if so desired

## Exercise 2: Further Exercism katas

Now, you can apply the same process to convert other Exercism katas into TypeScript!
