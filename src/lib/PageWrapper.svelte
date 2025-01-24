<script>
    export let backgroundColor = 'gray'; // Default background color
  </script>
  
  <style>
  :global(body) {
    margin: 0;
    padding: 0;
  }
  
    div {
      width: 100%;
      height: 100vh;
      padding:0px;
      margin:0px;
      background-color: var(--background-color);
      display: flex;
      justify-content: center; /* Center slot content horizontally */
      align-items: center;    /* Center slot content vertically */
    }
  </style>
  
  <div style="--background-color: {backgroundColor};">
    <slot></slot>
  </div>
  