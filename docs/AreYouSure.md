# AreYouSure Component

The `AreYouSure` component provides a two-step confirmation button with a safety mechanism to prevent accidental actions. The user has a chance to confirm their decision within a specified delay.

## Props

- **`buttonColor`** (string): Color of the initial button. Default: `"#007BFF"` (blue).
- **`textColor`** (string): Text color of the initial button. Default: `"#FFFFFF"` (white).
- **`warningColor`** (string): Color of the confirmation button. Default: `"#FF4136"` (red).
- **`warningTextColor`** (string): Text color of the confirmation button. Default: `"#FFFFFF"` (white).
- **`delay`** (number): Time (in seconds) the confirmation button remains visible. Default: `2`.
- **`initialText`** (string): Label for the initial button. Default: `"Delete"`.
- **`warningText`** (string): Label for the confirmation button. Default: `"Are you sure?"`.

## Usage

```svelte
<script>
  import AreYouSure from './AreYouSure.svelte';
</script>

<AreYouSure
  buttonColor="#4CAF50"
  textColor="#FFFFFF"
  warningColor="#F44336"
  warningTextColor="#FFFFFF"
  delay={3}
  initialText="Delete"
  warningText="Confirm Delete"
/>
```

## Behavior

1. **Initial Button**: Displays a button with `initialText` and `buttonColor`.
2. **Warning Button**: When the initial button is clicked, a second button with `warningText` and `warningColor` appears for the specified `delay` (in seconds).
3. **Execution**: Clicking the warning button executes the desired command and hides the button. If no action is taken within the `delay`, the warning button disappears.

## Customization

You can customize the appearance of the buttons using the provided props. Additionally, CSS variables (`--button-color`, `--text-color`, `--warning-color`, `--warning-text-color`) allow further styling directly in your project.

## Example Styling

```css
:global(button) {
  font-family: Arial, sans-serif;
  font-weight: bold;
}
```

## Notes

- This component is designed to be lightweight and does not depend on any external libraries.
- Ensure that the `handleSecondClick` function contains the logic for the action to be executed (e.g., deleting an item).

