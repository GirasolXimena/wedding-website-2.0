<script>
  import { Jumbotron } from "sveltestrap";
  import Button from "./Button.svelte";
  const handleClick = () => alert("I warned you!");
</script>

<style>
  .hero {
    background-color: black;
    height: 100vh;
    background-image: linear-gradient(rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0.75)),
      url("https://instagram.ffcm1-2.fna.fbcdn.net/vp/16a383f1d9b3a06d6972085e6cf7ae1d/5DFDB388/t51.2885-15/e35/41203721_691517357888913_5430100155676178400_n.jpg?_nc_ht=instagram.ffcm1-2.fna.fbcdn.net");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }
</style>

<div class="jumbotron hero text-center d-flex flex-column text-white">
  <h1 class="display-3">Hello, world!</h1>
  <p class="lead">
    This is a simple hero unit, a simple Jumbotron-style component for calling
    extra attention to featured content or information.
  </p>
  <p>
    It uses utility classes for typography and spacing to space content out
    within the larger container.
  </p>
  <Button onClick={handleClick} color="warning" buttonText="RSVP" />
</div>
