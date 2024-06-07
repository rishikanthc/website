<script>
	export let dot_size = '18px';
	export let label = '';
	export let x = 0;
	export let y = 0;
	export let font_size = '10px';
</script>

<div class="skill" style="position: absolute; top: {y}px; right: {x}px;">
	<div class="label" style="font-size: {font_size}">{label}</div>
	<div class="circle" style="width: {dot_size}; height: {dot_size};"></div>
</div>

<style>
	.skill {
		padding: 0;
		margin: 0;
		display: flex;
		flex-wrap: nowrap;
		align-items: center;
		width: fit-content;
		justify-content: center;
		gap: 5px;
		position: absolute;
	}
	.label {
		width: fit-content;
	}
	.circle {
		border-radius: 50%;
		border: 0.12em solid #af3029;
		background-color: #fff;
		width: 10px;
		height: 10px;
	}
</style>
