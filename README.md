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
