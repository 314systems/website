---
url: >-
  /docs/guide/usage/linter/rules/jsx_a11y/no-interactive-element-to-noninteractive-role.md
---

### What it does

Interactive HTML elements indicate controls in the user interface. Interactive elements include `<a href>`, `<button>`, `<input>`, `<select>`, `<textarea>`.

WAI-ARIA roles should not be used to convert an interactive element to a non-interactive element.
Non-interactive ARIA roles include `article`, `banner`, `complementary`, `img`, `listitem`, `main`, `region` and `tooltip`.

### Why is this bad?

Using a non-interactive role on an interactive element can confuse assistive technology users.

### Examples

Examples of **incorrect** code for this rule:

```jsx
<button role="img">Save</button>
```

Examples of **correct** code for this rule:

```jsx
<div role="img">
  <button>Save</button>
</div>
```

## Configuration

This rule accepts a configuration object with the following properties:

type: `object`

## How to use

## Version

This rule was added in vnext.

## References
