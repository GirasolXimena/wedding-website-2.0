<script>
  import { getContext } from "svelte";
  import ModalText from "./ModalText.svelte";
  import Button from "./Button.svelte";
  export let buttonText;
  export let message;

  const { open } = getContext("simple-modal");

  const onClick = () => {
    open(ModalText, { message });
  };
</script>

<Button color="primary" {onClick} {buttonText} />
