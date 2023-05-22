<script>
	import Card from '../../components/Card.svelte';
	import { cards } from '$lib/cards';
</script>

<h1 class="text-center">PRICES</h1>

<div class="flex flex-wrap">
	{#each cards as card}
		<div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 p-4">
			<Card title={card.title} description={card.description} imageUrl={card.imageUrl} />
		</div>
	{/each}
</div>
