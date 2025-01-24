# Anchor Component

The Anchor component is a lightweight, fully customizable link element designed for reusability across projects. It supports CSS variables for theming and passes through all valid HTML attributes.

---

## Features

1. **Customizable Theming**:
   - Uses CSS variables for colors and font size.
   - Defaults can be overridden by users.

2. **Dynamic Attributes**:
   - Supports additional attributes via `...$$restProps` (e.g., `id`, `aria-*`, `data-*`).

3. **Flexible Content**:
   - Allows custom content via a default slot.

4. **Scoped Styling**:
   - Encapsulated styles ensure no global conflicts.

---

## Usage

### Basic Example

```svelte
<script>
  import Anchor from './Anchor.svelte';
</script>

<Anchor href="/home">Home</Anchor>
```

### Custom Styling with CSS Variables

```html
<style>
  :root {
    --anchor-color: #ff5733;
    --anchor-hover-color: #c70039;
    --anchor-font-size: 1.2rem;
  }
</style>

<Anchor href="/about">About Us</Anchor>
```

### Passing Additional Attributes

```svelte
<Anchor href="/contact" id="contact-link" aria-label="Contact Us">
  Contact
</Anchor>
```

### Using Slots for Custom Content

```svelte
<Anchor href="/dashboard">
  <strong>Dashboard</strong>
</Anchor>
```

---

## Props

| Prop    | Type   | Default                | Description                     |
|---------|--------|------------------------|---------------------------------|
| `href`  | String | `"#"`                 | The URL to navigate to.         |
| `target`| String | `"_self"`            | Specifies where to open the link. |
| `rel`   | String | `"noopener noreferrer"` | Specifies the relationship of the target object. |

---

## Theming with CSS Variables

| Variable               | Default Value  | Description                        |
|------------------------|----------------|------------------------------------|
| `--anchor-color`       | `#007bff`      | The color of the anchor text.      |
| `--anchor-hover-color` | `#0056b3`      | The color on hover.                |
| `--anchor-font-size`   | `1rem`         | The font size of the anchor text.  |

---

## Notes

- Ensure to define CSS variables in your global styles to customize the theme.
- Test dynamic attributes and slots for your specific use case.