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
		DropdownDivider
	} from 'flowbite-svelte';
	import { onMount } from 'svelte';

	let currentPath = '';

	// используйте onMount для обновления переменной currentPath при загрузке компонента
	onMount(() => {
		currentPath = window.location.pathname;
	});

	function handleClick(event) {
		currentPath = event.target.pathname;
	}
</script>

<Navbar class="fixed top-0 w-full z-10" let:hidden let:toggle>
	<NavBrand href="/">
		<img
			src="https://flowbite.com/docs/images/logo.svg"
			class="mr-3 h-6 sm:h-9"
			alt="Flowbite Logo"
		/>
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
			LITUA.IO
		</span>
	</NavBrand>
	<NavHamburger on:click={toggle} />
	<NavUl {hidden}>
		<NavLi href="/" active={currentPath === '/'} on:click={handleClick}>HOME</NavLi>
		<NavLi href="/about" active={currentPath === '/about'} on:click={handleClick}>About</NavLi>
		<NavLi id="nav-menu1" class="cursor-pointer"><Chevron aligned>Services</Chevron></NavLi>
		<NavLi href="/prices" active={currentPath === '/prices'} on:click={handleClick}>Prices</NavLi>
		<NavLi href="/contact" active={currentPath === '/contact'} on:click={handleClick}>Contact</NavLi
		>
		<Dropdown triggeredBy="#nav-menu1" class="w-44 z-20">
			<DropdownItem href="/services/sites">Sites</DropdownItem>
			<DropdownItem href="/services/editing">Editing</DropdownItem>
		</Dropdown>
	</NavUl>
</Navbar>
