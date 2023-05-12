<script>
	import { DarkMode } from 'flowbite-svelte';
	import '../app.postcss';
	import Navbar from '../components/Navbar.svelte';
	import Footer from '../components/Footer.svelte';
</script>

<Navbar />
<DarkMode />
<main class="container mx-auto">
	<slot />
</main>
<Footer />
