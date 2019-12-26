<script>
  import {
    Collapse,
    Navbar,
    NavbarToggler,
    NavbarBrand,
    Nav,
    NavItem,
    NavLink
  } from "sveltestrap";
  import HeartLogo from "./HeartLogo.svelte";
  let isOpen = false;

  const handleUpdate = event => (isOpen = event.detail.isOpen);

  const NavLinks = [
    "How We Met",
    "Events",
    "Engagement",
    "Social",
    "Glimpse of the City",
    "Venue",
    "RSVP"
  ];
</script>

<Navbar class="text-white" color="warning" light expand="md">
  <NavbarBrand href="/">
    <HeartLogo />
    Robert & Mandi
  </NavbarBrand>
  <NavbarToggler on:click={() => (isOpen = !isOpen)} />
  <Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
    <Nav class="ml-auto" navbar>
      {#each NavLinks as link}
        <NavItem>
          <NavLink href="#{link.toLowerCase().replace(/\s/g, '')}">
            {link}
          </NavLink>
        </NavItem>
      {/each}
    </Nav>
  </Collapse>
</Navbar>
