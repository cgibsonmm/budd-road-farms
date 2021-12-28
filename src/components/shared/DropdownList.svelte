<script>
	export let links;
</script>

<div class="bg-gray-300">
	<ul>
		{#each links as item}
			<li class="p-2 text-lg">{item}</li>
		{/each}
	</ul>
</div>
