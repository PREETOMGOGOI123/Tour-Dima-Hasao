<script>
	import '../app.css';
	import Header from './Header.svelte';
	let { children } = $props();
</script>

<div class="overflow-hidden">
	<Header />
	
	{@render children()}
	
	<style>
	</style>
</div>