---
url: /docs/guide/usage/linter/rules/jsdoc/require-throws-description.md
---

### What it does

Requires a description for `@throws` tags.

### Why is this bad?

A `@throws` tag should explain the condition or reason an error may be thrown.

### Examples

Examples of **incorrect** code for this rule:

```js
/**
 * @throws {Error}
 */
function quux() {
  throw new Error("error");
}
```

Examples of **correct** code for this rule:

```js
/**
 * @throws {Error} Has a description
 */
function quux() {
  throw new Error("error");
}
```

## How to use

## Version

This rule was added in vnext.

## References
