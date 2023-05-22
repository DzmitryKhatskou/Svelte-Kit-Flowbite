<script>
	export let title;
	export let description;
	export let imageUrl;
</script>

<div
	class="hover:-translate-y-2 hover:scale-105 ease-in-out duration-600 transition-all shadow-lg rounded-lg overflow-hidden"
>
	<img class="w-full h-40 object-cover" src={imageUrl} alt="Course" />
	<div class="p-4">
		<h3 class="text-xl font-bold mb-2">{title}</h3>
		<p class="text-gray-700">{description}</p>
		<a href="#" class="block mt-3 text-sm font-semibold text-blue-500 hover:text-blue-600"
			>Learn More</a
		>
	</div>
</div>
