<script lang="ts">
	import Footer from '$lib/components/footer/footer.svelte';
	import Navigation from '$lib/components/navigation/navigation.svelte';
	import '../app.css';
	let { children } = $props();
</script>

<Navigation />
<section>
	{@render children()}
</section>
<Footer />
