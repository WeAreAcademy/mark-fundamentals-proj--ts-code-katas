---
module: mark-fundamentals

methods:
  - team
  - pair
  - solo

tags:
  - wip
---

# JS Code Katas

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a>

> This is part of Academy's [technical curriculum for **The Mark**](https://github.com/WeAreAcademy/curriculum-mark). All parts of that curriculum, including this project, are licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>.

You're now going to reinforce the TDD process and your JavaScript skills by completing a series of Exercism katas.

## Learning Outcomes

- Use a test-driven development process

## Exercise 1: Exercism Hello World - JavaScript

> 🎯 **Success criterion:** A completed and submitted version of the Exercism _Hello World_ problem

[Exercism](https://exercism.io/) has lots of exercises for a variety of challenges.

In this exercise, you'll complete the basic JavaScript Hello World challenge.

Exercism has a pretty good [Getting Started](https://exercism.io/getting-started) guide and documentation - see what you can do by following their guides!

Note that:

1. Exercism's using Jest's `describe` function to group together related tests (which helps for readability and organisation). We'll be doing this in future tests. You can [consult the Jest `describe` documentation](https://jestjs.io/docs/en/api#describename-fn) for more information.
2. Exercism's documentation suggests `npm install` and `npm test` - these are the equivalent of `yarn` and `yarn test`, respectively, which we've been using (you can use whichever; we suggest `yarn` for consistency).
3. Exercism's test files are using `.spec.js`; Jest recognises both `.test.js` and `.spec.js` files by default

## Exercise 2: Further Exercism challenges

At this point in time - one week into your full-time training! - we recommend working through the challenges labelled as 'Easy'.

If you completed [any previous Python Exercism katas](https://github.com/WeAreAcademy/mark-induction-proj--code-katas) we suggest that you redo them in JavaScript (as a way to notice similarities and differences between the the languages).

We also recommend trying to follow strict test-driven development (write a test for new behaviour/functionality before you write the code for it), and adding in your own custom tests for smaller helper functions that you write as part of your solution.

~3-5 Exercism katas is the number we suggest before moving on (so that you have sufficient comfort with JavaScript before starting TypeScript!).
