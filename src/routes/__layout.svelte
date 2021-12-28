<script>
	import Navbar from '../components/shared/Navbar.svelte';
</script>

<div>
	<Navbar />
	<slot />
</div>

<style global>
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
</style>
