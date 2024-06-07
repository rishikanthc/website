<script>
	import Dot from './dot.svelte';
	export let length = 100;
	export let dot_size = '5px';
	export let xaxis = false;
</script>

<div class="axis" class:xaxis>
	{#each Array(length) as _}
		<Dot {dot_size} />
	{/each}
</div>

<style>
	.axis {
		display: grid;
		gap: 2px;
	}
	.xaxis {
		grid-template-columns: repeat(100, 1fr);
		gap: 2px;
	}
</style>
