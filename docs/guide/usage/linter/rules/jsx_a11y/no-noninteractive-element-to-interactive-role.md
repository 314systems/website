---
url: >-
  /docs/guide/usage/linter/rules/jsx_a11y/no-noninteractive-element-to-interactive-role.md
---

### What it does

Non-interactive HTML elements indicate *content* and *containers* in the user interface.
Non-interactive elements include `<main>`, `<area>`, `<h1>` (through `<h6>`), `<p>`,
`<img>`, `<li>`, `<ul>`, and `<ol>`.

Interactive HTML elements indicate *controls* in the user interface.
Interactive elements include `<a href>`, `<button>`, `<input>`, `<select>`,
`<textarea>`.

[WAI-ARIA roles](https://www.w3.org/TR/wai-aria-1.1/#usage_intro) should not be used
to convert a non-interactive element to an interactive element. Interactive ARIA roles
include `button`, `link`, `checkbox`, `menuitem`, `menuitemcheckbox`,
`menuitemradio`, `option`, `radio`, `searchbox`, `switch`, and `textbox`.

### Why is this bad?

Overriding the semantic meaning of non-interactive elements with interactive roles
creates confusion for assistive technology users. The element lacks the expected
keyboard interaction patterns and focus management that interactive elements provide.

### Examples

Examples of **incorrect** code for this rule:

```jsx
<h1 role="button">Click me</h1>
<li role="link">Navigate</li>
<article role="button">Submit</article>
```

Examples of **correct** code for this rule:

```jsx
<button>Click me</button>
<a href="/page">Navigate</a>
<div role="button">Submit</div>
<ul role="menu"><li role="menuitem">Item</li></ul>
```

## Configuration

This rule accepts a configuration object with the following properties:

### allowed\_roles

type: `Record<string, array>`

A mapping of HTML element names to arrays of ARIA role strings that are
allowed overrides for that element. For example, `{ "ul": ["menu", "tablist"] }`
permits `<ul role="menu" />` without triggering the rule.

Defaults are:

```json
{
  "ul": ["menu", "menubar", "radiogroup", "tablist", "tree", "treegrid"],
  "ol": ["menu", "menubar", "radiogroup", "tablist", "tree", "treegrid"],
  "li": ["menuitem", "menuitemcheckbox", "menuitemradio", "row", "tab", "treeitem"],
  "fieldset": ["radiogroup", "presentation"]
}
```

## How to use

## Version

This rule was added in v1.64.0.

## References
