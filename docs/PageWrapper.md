# PageWrapper Component

The `PageWrapper` component provides a full-page layout with a customizable background color. It ensures content is centered both horizontally and vertically, making it ideal for simple page designs.

## Features
- Full viewport width and height.
- Default gray background with customizable color.
- Centers content using CSS Flexbox.
- Resets global `body` margin and padding for consistent layout.

## Props

### `backgroundColor` (optional)
- **Type**: `string`
- **Default**: `'gray'`
- **Description**: Sets the background color of the page. The value is applied via a CSS variable.

## CSS Variables

- `--background-color`: Defines the background color of the wrapper. Controlled by the `backgroundColor` prop.

## Usage

```svelte
<script>
  import PageWrapper from './PageWrapper.svelte';
</script>

<PageWrapper backgroundColor="lightblue">
  <h1>Welcome to My App</h1>
</PageWrapper>
```

## Notes
- The component resets the global `body` margin and padding to remove default browser spacing.
- Content inside the `<slot>` is automatically centered both vertically and horizontally.

