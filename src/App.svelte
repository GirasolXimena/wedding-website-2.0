<script>
  import Hero from "./components/Hero.svelte"; 
  import NavBar from './components/NavBar.svelte'
  import EventsList from './components/EventsList.svelte'
</script>

<svelte:head>
  <link
    rel="stylesheet"
    href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" />
</svelte:head>

<div>
  <NavBar /> 
  <Hero />
  <EventsList />
</div>
