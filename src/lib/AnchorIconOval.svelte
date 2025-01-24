<script>
  import Icons from './Icons.js';

  export let href = "#";
  export let target = "_self";
  export let rel = "noopener noreferrer";
  export let iconName = "ADD"; // Default icon name (restricted to names in Icons.js)

  let icon;

  // Fetch the icon using the provided name
  $: {
      if (Icons[iconName]) {
          icon = Icons[iconName];
      } else {
          console.warn(`Invalid icon name "${iconName}". Defaulting to "ADD".`);
          icon = Icons.ADD;
      }
  }
</script>

<a
  href={href}
  target={target}
  rel={rel}
  {...$$restProps}
  class="anchor-icon-oval"
>
  {#if icon}
    <span class="icon">{icon}</span>
  {/if}
  <slot></slot>
</a>

<style scoped>
  :root {
    --anchor-icon-oval-bg: #007bff;
    --anchor-icon-oval-hover-bg: #0056b3;
    --anchor-icon-oval-color: #ffffff;
    --anchor-icon-oval-padding: 8px 16px;
    --anchor-icon-oval-radius: 50px;
    --anchor-icon-oval-font-size: 1rem;
    --anchor-icon-spacing: 8px; /* Spacing between icon and text */
  }

  .anchor-icon-oval {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    background-color: var(--anchor-icon-oval-bg);
    color: var(--anchor-icon-oval-color);
    padding: var(--anchor-icon-oval-padding);
    border-radius: var(--anchor-icon-oval-radius);
    font-size: var(--anchor-icon-oval-font-size);
    text-decoration: none;
    transition: background-color 0.3s ease, color 0.3s ease;
  }

  .anchor-icon-oval:hover {
    background-color: var(--anchor-icon-oval-hover-bg);
  }

  .icon {
    margin-right: var(--anchor-icon-spacing);
    font-size: 1.2em;
    line-height: 1;
  }
</style>
