
### HdgWithIcon.md
```markdown
# HdgWithIcon

A heading component that displays an icon alongside the heading text.

## Props

- `text` (string, required): The text of the heading.
- `iconName` (string, required): The name of the icon from the `Icons.js` file.
- `level` (number, optional): The heading level (`1` to `6`). Default: `1`.
- `color` (string, optional): The CSS color of the icon and text. Default: `--color-primary`.

## Usage

```svelte
<script>
  import HdgWithIcon from './HdgWithIcon.svelte';
</script>

<HdgWithIcon text="My Heading" iconName="star" level={2} color="var(--color-secondary)" />
