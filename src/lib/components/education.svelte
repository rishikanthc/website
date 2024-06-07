<script>
	import Degrees from '$lib/components/degrees.svelte';
	import SectionTitle from '$lib/components/sectionTitle.svelte';
</script>

<div class="edu">
	<SectionTitle val="EDUCATION" />
	<Degrees />
</div>

<style>
	.edu {
		display: flex;
		flex-direction: column;
		align-items: top;
		width: fit-content;
		justify-content: center;
		gap: 1.5em;
	}
</style>
