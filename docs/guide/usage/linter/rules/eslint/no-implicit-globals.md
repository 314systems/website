---
url: /docs/guide/usage/linter/rules/eslint/no-implicit-globals.md
---

### What it does

Disallows declarations in the global scope, global variable leaks, and
writes or redeclarations of read-only globals.

### Why is this bad?

Browser scripts share a global scope. Top-level `var` and `function`
declarations, and assignments to undeclared variables in sloppy mode,
create globals that can collide with other scripts.

### Examples

Examples of **incorrect** code for this rule:

```js
var foo = 1;
function bar() {}
baz = 1;
```

Examples of **correct** code for this rule:

```js
window.foo = 1;
(function () {
  var bar = 1;
})();
```

## Configuration

### lexicalBindings

type: `boolean`

default: `false`

## How to use

## Version

This rule was added in vnext.

## References
