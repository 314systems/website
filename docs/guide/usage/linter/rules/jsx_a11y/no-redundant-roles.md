---
url: /docs/guide/usage/linter/rules/jsx_a11y/no-redundant-roles.md
---

### What it does

Enforces that code does not include a redundant `role` property, in the
case that it's identical to the implicit `role` property of the
element type.

### Why is this bad?

Redundant roles can lead to confusion and verbosity in the codebase.

### Examples

This rule applies for the following elements and their implicit roles:

* `<nav>`: `navigation`
* `<button>`: `button`
* `<main>`: `main`

Examples of **incorrect** code for this rule:

```jsx
<nav role="navigation"></nav>
<button role="button"></button>
<main role="main"></main>
```

Examples of **correct** code for this rule:

```jsx
<nav></nav>
<button></button>
<main></main>
```

## How to use

## Version

This rule was added in v0.2.1.

## References
