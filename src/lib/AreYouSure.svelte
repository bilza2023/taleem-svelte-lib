<script>
  export let buttonColor = "#007BFF"; // Default blue color
  export let textColor = "#FFFFFF"; // Default white text color
  export let warningColor = "#FF4136"; // Default red warning color
  export let warningTextColor = "#FFFFFF"; // Default white warning text color
  export let delay = 2; // Default delay in seconds

  export let initialText = "Delete"; // Text for the first button
  export let warningText = "Are you sure?"; // Text for the warning button

  let showWarning = false;
  let timeoutId;

  const handleFirstClick = () => {
    showWarning = true;
    timeoutId = setTimeout(() => {
      showWarning = false;
    }, delay * 1000);
  };

  const handleSecondClick = () => {
    showWarning = false;
    clearTimeout(timeoutId);
    // Execute the desired command here
    console.log("Command executed");
  };
</script>

<style>
  button {
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 1rem;
    transition: background-color 0.3s ease;
  }

  .initial {
    background-color: var(--button-color, #007BFF);
    color: var(--text-color, #FFFFFF);
  }

  .warning {
    background-color: var(--warning-color, #FF4136);
    color: var(--warning-text-color, #FFFFFF);
  }
</style>

{#if !showWarning}
  <button
    class="initial"
    style="--button-color: {buttonColor}; --text-color: {textColor};"
    on:click={handleFirstClick}
  >
    {initialText}
  </button>
{:else}
  <button
    class="warning"
    style="--warning-color: {warningColor}; --warning-text-color: {warningTextColor};"
    on:click={handleSecondClick}
  >
    {warningText}
  </button>
{/if}