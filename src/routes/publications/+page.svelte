<script>
	import Award from '$lib/icons/award.svelte';
	export const pubs = [
		{
			title:
				'A Neuro-Symbolic Architecture for Efficient Classification using Hyperdimensional Computing',
			auth: 'Rishikanth Chandrasekaran, Tajana Rosing',
			venue: 'ISLPED',
			date: 2024
		},
		{
			title: 'Federated Hyperdimensional Computing',
			auth: 'Kazim Ergun, Rishikanth Chandrasekaran, Tajana Rosing',
			venue: 'ACM TIoT (under review)',
			date: 2023
		},
		{
			title: 'Multi-label classification with Hyperdimensional Representations',
			auth: 'Rishikanth Chandrasekaran, F Asgareinjad, J Morris, T Rosing',
			venue: 'IEEE Access Journal',
			date: 2023
		},
		{
			title: 'Fhdnn: Communication efficient and robust federated learning for aiot networks',
			auth: 'R Chandrasekaran, K Ergun, J Lee, D Nanjunda, J Kang, T Rosing',
			venue: 'Proceedings of the 59th ACM/IEEE Design Automation Conference',
			date: 2022
		},
		{
			title:
				'Hdnn-pim: Efficient in memory design of hyperdimensional computing with feature extraction',
			auth: 'A Dutta, S Gupta, B Khaleghi, R Chandrasekaran, W Xu, T Rosing',
			venue: 'Proceedings of the Great Lakes Symposium on VLSI',
			date: 2022
		},
		{
			title: 'A drone-based system for intelligent and autonomous homes',
			auth: 'S Xia, R Chandrasekaran, Y Liu, C Yang, TS Rosing, X Jiang',
			venue: 'Proceedings of the 19th ACM Conference on Embedded Networked Sensor Systems',
			date: 2021,
			award: 'Best Demo'
		},
		{
			title: 'Efficient Sparse Processing for Smart Home Applications',
			auth: 'Rishikanth Chandrasekaran, Yunhui Guo, Anthony Thomas, Masimiliano Menarini, Michael Ostertag, Tajana Rosing',
			venue: 'ACM Conference on Embedded Network Sensor Systems (SenSys)',
			date: 2019
		},
		{
			title:
				'A Scalable System for Apportionment and Tracking of Energy Footprints in Commercial Buildings',
			auth: 'Peter Wei, Xiaoqi Chen, Jordan Vega, Stephen Xia, Rishikanth Chandrasekaran, Xiaofan Jiang',
			venue: 'ACM Transaction on Sensor Networks (TSON)',
			date: 2018
		},
		{
			title: 'PAWS: A Wearable Acoustic System for Pedestrian Safety',
			auth: 'Daniel de Godoy, Bashima Islam, Stephen Xia, Md Tamzeed Islam, Rishikanth Chandrasekaran, Yen-Chun Chen, Shahriar Nirjon, Peter R Kinget, Xiaofan Jiang',
			venue: 'Internet-of-Things Design and Implementation (IoTDI)',
			date: 2018
		},
		{
			title: 'Paws: A wearable acoustic system for pedestrian safety.',
			venue:
				'IEEE/ACM Third International Conference on Internet-of-Things Design and Implementation (IoTDI)',
			date: 2018,
			auth: 'Daniel de Godoy, Bashima Islam, Stephen Xia, Md Tamzeed Islam, Rishikanth Chandrasekaran, Yen-Chun Chen, Shahriar Nirjon, Peter R Kinget, Xiaofan Jiang'
		},
		{
			title:
				'ePrints a real-time and scalable system for fair apportionment and tracking of personal energy footprints in commercial buildings',
			venue:
				'ACM International Conference on Systems for Energy-Efficient Built Environments (BuildSys)',
			auth: 'P Wei, X Chen, J Vega, S Xia, R Chandrasekaran, X Jiang',
			date: 2017,
			award: 'Best Paper Runner Up'
		},
		{
			title: 'Adaptive and Personalized Energy Saving Suggestions for Occupants in Smart Buildings',
			venue:
				'ACM International Conference on Systems for Energy-Efficient Built Environments (BuildSys)',
			auth: 'P Wei, X Chen, R Chandrasekaran, F Song, X Jiang',
			date: 2016,
			award: 'Best Poster'
		},
		{
			title:
				'SEUS: A Wearable Multi-Channel Acoustic Headset Platform to Improve Pedestrian Safety',
			venue: 'ACM Conference on Embedded Network Sensor Systems (SenSys)',
			auth: 'R Chandrasekaran, D de Godoy, S Xia, MT Islam, B Islam, S Nirjon, P Kinget, X Jiang',
			date: 2016
		},
		{
			title: 'Personal energy footprint in shared building environment',
			venue: 'International Conference on Information Processing in Sensor Networks (IPSN)',
			auth: 'P Wei, X Chen, R Chandrasekaran, F Song, X Jiang',
			date: 2016
		},
		{
			title:
				'Low-cost intelligent gesture recognition engine for audio-vocally impaired individuals',
			venue: 'Global Humanitarian Technology Conference (GHTC)',
			auth: 'C Rishikanth, H Sekar, G Rajagopal, R Rajesh, V Vijayaraghavan',
			date: 2014
		}
	];
</script>

<div class="front">
	{#each pubs as pub (pub.title)}
		<div class="item">
			<div class="left">
				<div class="title">{pub.title}</div>
				<div class="authors">{pub.auth}</div>
				<div class="venue">{pub.venue}</div>
				{#if pub.award}
					<div class="award">
						<div class="icon">
							<Award size="24" starColor="#ffbd59" />
						</div>
						<div class="name">{pub.award}</div>
					</div>
				{/if}
			</div>
			<div class="right">
				{pub.date}
			</div>
		</div>
	{/each}
</div>

<style>
	.front {
		display: flex;
		flex-direction: column;
		gap: 2.5em;
	}
	.item {
		box-shadow: 0 1px 3px hsla(0, 0%, 0%, 0.2);
		padding: 1em;
		border-radius: 5px;
		display: flex;
		gap: 10em;
		justify-content: space-between;
	}
	.award {
		display: flex;
		align-items: center;
		margin-top: 0.25em;
		gap: 0.25em;
	}
	.name {
		color: #a02f6f;
		color: #bb100a;
		font-size: 16px;
	}
	.right {
		font-size: 18px;
		/*color: #205ea6;*/
		color: #5371ff;
		color: #1f60c2;
		font-family: Montserrat, sans-serif;
	}
	.authors {
		font-style: italic;
		/*color: #5e409d;*/
		color: #1f60c2;
		font-size: 16px;
	}
	.title {
		font-size: 20px;
		/*color: #343331;*/
		color: #575653;
	}
	.venue {
		font-size: 14px;
		font-weight: 300;
	}
	@media (min-width: 1280px) {
		.front {
			margin-left: 35%;
		}
	}
	@media (min-width: 710px) {
		.front {
			margin-top: 5em;
		}
	}
</style>
