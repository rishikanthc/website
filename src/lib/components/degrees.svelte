<script>
	const edu = [
		{
			degree: 'PhD',
			uni: 'University of California, San Diego',
			year: 2024,
			dep: 'Computer Science'
		},
		{
			degree: 'Masters',
			uni: 'Columbia University',
			year: 2017,
			loc: 'NYC',
			dep: 'Computer Engineering'
		},
		{
			degree: 'Bachelors',
			uni: 'Anna University',
			year: 2015,
			loc: 'INDIA',
			dep: 'Electrical & Electronics Engineering'
		}
	];
</script>

<div class="education-grid">
	{#each edu as e}
		<div class="edu-grid">
			<div class="left">
				<div class="degree">{e.degree} in {e.dep}</div>
				<div class="row">
					<div class="uni">{e.uni}</div>
					<div class="loc">
						{#if e.loc}{e.loc}{/if}
					</div>
				</div>
			</div>
			<div class="year">{e.year}</div>
		</div>
	{/each}
</div>

<style>
	.education-grid {
		display: grid;
		gap: 2em;
		margin: 0;
		padding: 0;
		width: fit-content;
	}
	.edu-grid {
		display: grid;
		grid-template-columns: 4fr 1fr;
		gap: 2em;
		justify-content: space-between;
		align-items: center;
	}
	.left {
		font-size: 16px;
	}
	.year {
		font-size: 16px;
		color: #205ea6;
		width: fit-content;
		margin: 0 auto;
	}
	.loc {
		font-size: 10px;
		color: #24837b;
	}
	.row {
		display: flex;
		align-items: end;
		gap: 0.25em;
	}
	.uni {
		color: #6f6e69;
	}
	@media (min-width: 1920px) {
		.left {
			font-size: 18px;
		}
		.year {
			font-size: 20px;
			color: #205ea6;
		}
		.loc {
			font-size: 10px;
			color: #24837b;
		}
	}
</style>
