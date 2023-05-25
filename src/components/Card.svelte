<script>
	export let title;
	export let description;
	export let imageUrl;
</script>

<div
	class="dark:bg-[#34455d] bg-slate-50 hover:-translate-y-2 duration-500 shadow-2xl hover:scale-105 ease-in-out transition-all rounded-lg overflow-hidden"
>
	<img class="w-full h-40 object-cover" src={imageUrl} alt="Course" />
	<div class="p-4">
		<h3 class="text-xl font-bold mb-2">{title}</h3>
		<p class="text-gray-500">{description}</p>
		<a href="#" class="block mt-3 text-sm font-semibold text-blue-500 hover:text-blue-600"
			>Learn More</a
		>
	</div>
</div>
