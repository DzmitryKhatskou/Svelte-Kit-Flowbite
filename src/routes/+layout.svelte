<script>
	import { DarkMode } from 'flowbite-svelte';
	import '../app.postcss';
	import Navbar from '../components/Navbar.svelte';
	import Footer from '../components/Footer.svelte';
</script>

<Navbar />
<DarkMode />
<main
	class=" max-w-[90%] px-10
  mx-auto"
>
	<slot />
</main>
<Footer />
