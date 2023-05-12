<script>
  import {
    Navbar,
    NavBrand,
    NavLi,
    NavUl,
    NavHamburger,
    Dropdown,
    DropdownItem,
    Chevron,
    DropdownDivider,
  } from "flowbite-svelte";
</script>

<Navbar let:hidden let:toggle>
  <NavBrand href="/">
    <img
      src="https://flowbite.com/docs/images/logo.svg"
      class="mr-3 h-6 sm:h-9"
      alt="Flowbite Logo"
    />
    <span
      class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
    >
      LITUA.IO
    </span>
  </NavBrand>
  <NavHamburger on:click={toggle} />
  <NavUl {hidden}>
    <NavLi href="/" active={true}>HOME</NavLi>
    <NavLi id="nav-menu1" class="cursor-pointer"
      ><Chevron aligned>Services</Chevron></NavLi
    >

    <NavLi href="/prices">Prices</NavLi>
    <NavLi href="/contact">Contact</NavLi>
    <Dropdown triggeredBy="#nav-menu1" class="w-44 z-20">
      <DropdownItem href="/services/sites">Sites</DropdownItem>
      <DropdownItem href="/services/editing">Editing</DropdownItem>
    </Dropdown>
  </NavUl>
</Navbar>
