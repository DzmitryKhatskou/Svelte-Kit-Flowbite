<script>
	import { DarkMode } from 'flowbite-svelte';
	import '../app.postcss';
	import Navbar from '../components/Navbar.svelte';
	import Footer from '../components/Footer.svelte';
</script>

<Navbar />
<DarkMode class="fixed top-[68px] md:top-20 left-2" />
<main
	class="flex flex-col py-20 mt-[60px] md:mt-[72px] justify-center items-center max-w-[90%] px-10
	  mx-auto"
>
	<slot />
</main>
<Footer />
