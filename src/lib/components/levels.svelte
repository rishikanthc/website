<script>
	import Circle2 from '$lib/icons/circle2.svelte';
	import Halfcircle from '$lib/icons/halfcircle.svelte';
	export let level = 5;
	export let size = 18;
	export let size2 = '1.1em';
	export let half = true;
</script>

<div class="level">
	{#each Array(level) as _}
		<Circle2 width={size} iconColor="#0e61fe" />
	{/each}

	{#if half}
		<Halfcircle width={size2} iconColor="#0e61fe" />
	{/if}

	{#if level < 5 && half}
		{#each Array(5 - 1 - level) as _}
			<div class="circle" style="width: {size - 5}px; height: {size - 5}px;"></div>
		{/each}
	{:else if level < 5}
		{#each Array(5 - level) as _}
			<div class="circle" style="width: {size - 5}px; height: {size - 5}px;"></div>
		{/each}
	{/if}
</div>

<style>
	.level {
		width: fit-content;
		display: flex;
		align-items: center;
	}
	.circle {
		margin: 2px;
		border-radius: 50%;
		border: 0.12em solid #205ea6;
		background-color: #fff;
	}
</style>
