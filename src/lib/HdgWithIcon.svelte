<script>
  import Icons from './Icons.js';

  export let iconName = "ADD"; // Default icon name

  export let text = "Heading"; // Default heading text
  export let fontSize = "1.5rem"; // Default font size
  export let backgroundColor = "red"; // Default background color
  export let textColor = "#000000"; // Default text color
  export let textAlign = "left"; // Default text alignment

  let icon;
  // Validate if the provided icon is from Icons
  $: {
    if (Icons[iconName]) {
        icon = Icons[iconName];
    } else {
        console.warn(`Invalid icon name "${iconName}". Defaulting to "ADD".`);
        icon = Icons.ADD;
    }
}

</script>

<style>
  .heading-container {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.5rem;
    border-radius: 4px;
    transition: background-color 0.3s ease;
  }

  .icon {
    display: inline-block;
    font-size: inherit;
  }

  .heading {
    font-size: inherit;
    color: inherit;
    text-align: inherit;
    flex-grow: 1;
  }
</style>

<div
  class="heading-container"
  style="
    font-size: {fontSize};
    background-color: {backgroundColor};
    color: {textColor};
    text-align: {textAlign};
  "
>
  <span class="icon">{icon}</span>
  <div class="heading">{text}</div>
</div>
