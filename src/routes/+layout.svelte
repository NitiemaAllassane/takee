<script lang="ts">
	import Sidebar from '$lib/components/Sidebar.svelte';
	import '../app.css';

	let { children } = $props();
</script>


<div class=" grid grid-cols-[1fr_3fr] ">
	<Sidebar  />
	<main>
		<div class="container">
			{@render children()}
		</div>
	</main>
</div>

