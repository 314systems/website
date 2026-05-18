---
url: /docs/guide/usage/linter/rules/jsdoc/require-yields-type.md
---

### What it does

Requires a type on the `@yields` tag.

### Why is this bad?

A `@yields` tag should document the type yielded by the generator.

### Examples

Examples of **incorrect** code for this rule:

```js
/** @yields */
function* quux() {}
```

Examples of **correct** code for this rule:

```js
/** @yields {string} */
function* quux() {}
```

## How to use

## Version

This rule was added in vnext.

## References
