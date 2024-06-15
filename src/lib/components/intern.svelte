<script>
	import SectionTitle from '$lib/components/sectionTitle.svelte';

	const experience = [
		{
			org: 'ARM Research',
			loc: 'Austin, Texas (Remote)',
			title: 'Research Intern',
			when: "Summer'21",
			details: {
				descr:
					'Developed Deep Learning models to predict malicious code from hardware performance counters. Assisted in developing methods for identifying models polluted by adverseries',
				highlights:
					'Secured a Patent for detecting unknown-unknowns in Time Series Forecasting applications'
			}
		},
		{
			org: 'Huawei',
			title: 'Mobile Sensing Intern',
			loc: 'Santa Clara, California',
			when: "Summer'18",
			details: {
				descr:
					'Designed Fast Machine Learning algorithms for inertial activity recognition using smartphone. Provided optimized implementation for real-time activity recognition on smartphones.',
				highlights: 'Deployed in production on smartphones'
			}
		}
	];
</script>

<div class="intern">
	<div class="section-tit">
		<SectionTitle val="INTERNSHIPS" />
	</div>
	<div class="items">
		{#each experience as exp (exp.org)}
			<div class="item">
				<div class="meta">
					<div class="role">
						<div class="org">{exp.org}</div>
						<div class="title">{exp.title}</div>
					</div>
					<div class="logis">{exp.when}</div>
				</div>
				<div class="desc">
					<p>{exp.details.descr}</p>
					<p class="highlight">{exp.details.highlights}</p>
				</div>
			</div>
		{/each}
	</div>
</div>

<style>
	.intern {
		display: flex;
		flex-direction: column;
		align-items: left;
		gap: 1.5rem;
		width: fit-content;
		/*margin-top: 4em;*/
	}
	.item,
	.role {
		display: grid;
	}
	.item {
		align-items: center;
		justify-content: left;
		width: fit-content;
	}
	.role {
		justify-content: left;
		align-items: center;
		width: fit-content;
	}

	.items {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: start;
		gap: 1em;
		width: fit-content;
	}
	.meta {
		display: grid;
		gap: 1em;
		grid-template-columns: 3fr 1fr;
		width: fit-content;
	}
	.highlight {
		font-style: italic;
		color: #24837b;
		color: #00c2bf;
		width: fit-content;
	}
	.logis {
		color: #205ea6;
		color: #0e61fe;
		color: #4589ff;
		width: fit-content;
	}
	.org {
		font-size: 18px;
		color: #d14d41;
		color: #d62c6f;
		width: fit-content;
	}
	.title {
		font-style: italic;
		width: fit-content;
	}
	.desc {
		line-height: 1.6;
		width: fit-content;
		color: #6f6e69;
		color: #c6c6c6;
	}

	@media (min-width: 710px) {
	}
</style>
