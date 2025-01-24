# AnchorIconOval

A clickable anchor component with an oval icon for visual emphasis.

## Props

- `href` (string, required): The URL to navigate to when the anchor is clicked.
- `iconName` (string, required): The name of the icon from the `Icons.js` file.
- `size` (string, optional): The size of the oval (e.g., `small`, `medium`, `large`). Default: `medium`.
- `color` (string, optional): The CSS color of the oval. Default: `--color-primary`.

## Usage

```svelte
<script>
  import AnchorIconOval from './AnchorIconOval.svelte';
</script>

<AnchorIconOval href="/example" iconName="check" size="large" color="var(--color-accent)" />
