<script>
	import {
		Footer,
		FooterCopyright,
		FooterLinkGroup,
		FooterBrand,
		FooterLink
	} from 'flowbite-svelte';
</script>

<Footer class="border-t border-gray-600 fixed bottom-0 left-0 right-0 w-full" footerType="logo">
	<div class="sm:flex sm:items-center sm:justify-between">
		<FooterBrand
			href="https://flowbite.com"
			src="https://flowbite.com/docs/images/logo.svg"
			alt="Flowbite Logo"
			name="LITUA.IO"
		/>
		<FooterLinkGroup
			ulClass="flex flex-wrap items-center mb-6 text-sm text-gray-500 sm:mb-0 dark:text-gray-400"
		>
			<FooterLink href="/">About</FooterLink>
			<FooterLink href="/">Privacy Policy</FooterLink>
			<FooterLink href="/">Licensing</FooterLink>
			<FooterLink href="/">Contact</FooterLink>
		</FooterLinkGroup>
	</div>
	<hr class="my-6 border-gray-300 sm:mx-auto dark:border-gray-700 lg:my-8" />
	<FooterCopyright href="/" by="Flowbite™" />
</Footer>
