<script>
  import { Button } from "sveltestrap";
  export let color;
  export let onClick;
  export let buttonText;
</script>

<Button on:click={onClick} class="mt-auto align-self-center px-5 py-2" {color}>
  {buttonText}
</Button>
