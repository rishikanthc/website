<script>
	import SectionTitle from './sectionTitle.svelte';
	import Axis from './axis.svelte';
	import Point from './point.svelte';

	const skills = [
		{ label: 'Deep Learning', x: 100, y: 100 },
		{ label: 'Time Series Forecasting', x: 75, y: 68 },
		{ label: 'Image Classification', x: 80, y: 82 },
		{ label: 'Federated Learning', x: 90, y: 75 },
		{ label: 'Text Classification', x: 50, y: 75 },
		{ label: 'Computer Vision', x: 55, y: 62 },
		{ label: 'Hyperdimensional Computing', x: 95, y: 95 },
		{ label: 'TinyML', x: 90, y: 90 },
		{ label: 'Bayesian Learning', x: 65, y: 55 },
		{ label: 'Causal Learning', x: 60, y: 50 },
		{ label: 'Generative Learning', x: 50, y: 40 }
	];
</script>

<div class="skills">
	<SectionTitle val="SKILLS" />
	<div class="graph">
		<div class="graph_area">
			<Axis dot_size="2px" xaxis={false} />
			<div class="graph-plane">
				{#each skills as skill (skill.label)}
					<Point
						label={skill.label}
						font_size="16px"
						dot_size="8px"
						x={400 - 4 * skill.x}
						y={400 - 4 * skill.y}
					/>
				{/each}
			</div>
		</div>
		<Axis dot_size="2px" xaxis={true} />
	</div>
</div>

<style>
	.skills {
		display: flex;
		align-items: center;
		justify-content: left;
		height: fit-content;
		padding: 0;
		margin: 0;
	}
	.graph-plane {
		width: 400px;
		height: 400px;
		padding: 0;
		position: relative;
	}
	.graph_area {
		display: flex;
		width: 400px;
		height: 400px;
	}
	.graph {
		display: grid;
		grid-template-columns: 1fr;
		justify-content: center;
	}
</style>
