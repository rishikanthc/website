<script>
	export let val = '';
</script>

<div class="heading">{val}</div>

<style>
	.heading {
		font-family: Montserrat, sans-serif;
		/*font-weight: bold;*/
		font-size: 20px;
		/*transform-origin: 50% 50%;*/
		/*transform: rotate(-90deg);*/
		white-space: nowrap;
		/*height: 50px;*/
		/*height: 16px;*/
		letter-spacing: 4px;
		/*color: #100f0f;*/
		color: #f4f4f4;
		padding: 0;
		/*border-bottom: 1px solid #ffbd59;*/
		/*border-bottom: 1px solid #525252;*/
		padding-bottom: 8px;
	}
	@media (min-width: 710px) {
		.heading {
			font-size: 22px;
			height: 20px;
		}
	}
</style>
