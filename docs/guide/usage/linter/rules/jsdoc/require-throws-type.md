---
url: /docs/guide/usage/linter/rules/jsdoc/require-throws-type.md
---

### What it does

Requires a type on the `@throws` tag.

### Why is this bad?

A `@throws` tag should document the type of error that may be thrown.

### Examples

Examples of **incorrect** code for this rule:

```js
/** @throws */
function quux() {
  throw new Error("error");
}
```

Examples of **correct** code for this rule:

```js
/** @throws {Error} */
function quux() {
  throw new Error("error");
}
```

## How to use

## Version

This rule was added in vnext.

## References
