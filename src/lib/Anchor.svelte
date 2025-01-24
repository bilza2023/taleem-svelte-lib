<script>
    export let href = "#";
    export let target = "_self";
    export let rel = "noopener noreferrer";
  </script>
  
  <a
    href={href}
    target={target}
    rel={rel}
    {...$$restProps}
    class="anchor"
  >
    <slot>Link</slot>
  </a>
  
  <style scoped>
    :root {
      --anchor-color: #007bff;
      --anchor-hover-color: #0056b3;
      --anchor-font-size: 1rem;
    }
  
    .anchor {
      color: var(--anchor-color);
      font-size: var(--anchor-font-size);
      text-decoration: none;
      transition: color 0.3s ease;
    }
  
    .anchor:hover {
      color: var(--anchor-hover-color);
    }
  </style>
  