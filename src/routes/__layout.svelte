<script>
	import Navbar from '../components/shared/Navbar.svelte';
</script>

<div class="bg-gray-100 h-screen">
	<Navbar />
	<div class="container">
		<slot />
	</div>
</div>

<style global>
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
</style>
