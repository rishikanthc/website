<script>
	import SectionTitle from '$lib/components/sectionTitle.svelte';
	import Award from '$lib/icons/award.svelte';

	const awards = [
		{
			name: 'Best Demo Award',
			event: 'SenSys',
			year: '2022'
		},
		{
			name: 'Best Paper Runner Up',
			event: 'BuildSys',
			year: '2017'
		},
		{
			name: 'Best Poster Award',
			event: 'BuildSys',
			year: '2017'
		},
		//{
		//	name: 'Best use of AWS',
		//	event: 'HackRU',
		//	year: '2017'
		//},
		{
			name: 'Best Demo Runner Up',
			event: 'SenSys',
			year: '2016'
		},
		{
			name: 'Google Research Pilot Award',
			event: '',
			year: '2016'
		},
		//{
		//	name: 'Best Dev Tool Award',
		//	event: 'HackRU',
		//	year: '2016'
		//},
		{
			name: 'Best Poster Award',
			event: 'MIT IoT',
			year: '2014'
		}
		//{
		//	name: 'Winner',
		//	event: 'MIT IoT Hackathon',
		//	year: '2014'
		//}
	];
</script>

<div class="outer">
	<div class="awards-flex-cont">
		<SectionTitle val="AWARDS" />
		<div class="rows">
			{#each awards as award}
				<div class="row">
					<div class="star"><Award size="28" starColor="#ffc200" /></div>
					<div class="award">{award.name}</div>
					<div class="sep">|</div>
					<div class="event">{award.event}</div>
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
	.awards-flex-cont {
		display: flex;
		flex-direction: column;
		align-items: left;
		justify-content: center;
		width: fit-content;
		gap: 1.5em;
	}
	.rows {
		display: flex;
		flex-direction: column;
		gap: 0.8em;
		justify-content: center;
		align-items: start;
		width: fit-content;
	}

	.row {
		display: flex;
		gap: 0;
		align-items: center;
		justify-content: center;
		gap: 8px;
		width: fit-content;
	}
	.award {
		font-size: 18px;
	}
	.event {
		font-size: 14px;
		color: #575653;
	}
	.sep {
		width: 2px;
		font-size: 10px;
		background-color: #205ea6;
		color: #205ea6;
	}
</style>
