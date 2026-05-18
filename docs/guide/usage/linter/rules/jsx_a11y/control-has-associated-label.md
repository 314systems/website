---
url: /docs/guide/usage/linter/rules/jsx_a11y/control-has-associated-label.md
---

### What it does

Enforce that a control (an interactive element) has a text label.

### Why is this bad?

An interactive element (such as a `<button>`) without an accessible
text label makes it difficult or impossible for users of assistive
technologies to understand the purpose of the control.

### Examples

Examples of **incorrect** code for this rule:

```jsx
<button />
<input type="text" />
<a href="/path" />
<th />
<div role="button" />
<div role="checkbox" />
```

Examples of **correct** code for this rule:

```jsx
<button>Save</button>
<button aria-label="Save" />
<label>Name <input type="text" /></label>
<a href="/path">Learn more</a>
<th>Column Header</th>
<div role="button">Submit</div>
<div role="checkbox" aria-labelledby="label_id" />
```

## Configuration

This rule accepts a configuration object with the following properties:

### controlComponents

type: `string[]`

default: `[]`

Custom JSX components to be treated as interactive controls.

### depth

type: `integer`

default: `2`

Maximum depth to search for an accessible label within the element.
Defaults to `2`.

### ignoreElements

type: `string[]`

default: `[]`

Elements to ignore (in addition to the default ignore list).
Defaults to `[]`.

### ignoreRoles

type: `string[]`

default: `[]`

Interactive roles to ignore.
Defaults to `[]`.

### labelAttributes

type: `string[]`

default: `[]`

Additional attributes to check for accessible label text.

## How to use

## Version

This rule was added in vnext.

## References
