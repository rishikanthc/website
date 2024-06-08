<script>
	import SectionTitle from './sectionTitle.svelte';
	import Axis from './axis.svelte';
	import Point from './point.svelte';
	import Levels from './levels.svelte';

	const skills = [
		{ label: 'Deep Learning', x: 100, y: 100, level: 5, half: false },
		{ label: 'Time Series Forecasting', x: 75, y: 68, level: 4, half: false },
		{ label: 'Image Classification', x: 80, y: 82, level: 4, half: true },
		{ label: 'Federated Learning', x: 90, y: 75, level: 4, half: true },
		{ label: 'Text Classification', x: 50, y: 75, level: 4, half: false },
		{ label: 'Computer Vision', x: 55, y: 62, level: 3, half: false },
		{ label: 'Hyperdimensional Computing', x: 95, y: 95, level: 5, half: false },
		{ label: 'TinyML', x: 90, y: 90, level: 4, half: false },
		{ label: 'Bayesian Learning', x: 65, y: 55, half: true, level: 3 },
		{ label: 'Causal Learning', x: 60, y: 50, level: 2, half: true },
		{ label: 'Generative Learning', x: 50, y: 40, level: 2, half: true }
	];
</script>

<div class="outer">
	<div class="skills">
		<SectionTitle val="SKILLS" />
		<div class="panel">
			{#each skills as skill (skill.label)}
				<div class="level">
					<div class="label">{skill.label}</div>
					<Levels size="14" level={skill.level} half={skill.half} />
				</div>
			{/each}
		</div>
	</div>
</div>

<style>
	.outer {
		display: grid;
		/*justify-content: center;*/
	}
	.skills {
		display: flex;
		flex-direction: column;
		align-items: left;
		justify-content: center;
		height: fit-content;
		gap: 1.5rem;
		padding: 0;
		margin: 0;
		width: fit-content;
	}
	.panel {
		display: grid;
		gap: 1em;
	}
	.level {
		display: grid;
		grid-template-columns: 3fr 1fr;
		gap: 2em;
	}
	.label {
		font-size: 16px;
	}
</style>
