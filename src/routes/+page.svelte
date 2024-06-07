<script>
	import Logo from '$lib/icons/logo.svelte';
	import Intro from '$lib/components/intro.svelte';
	import Education from '$lib/components/education.svelte';
	import Awards from '$lib/components/awards.svelte';
	import Intern from '$lib/components/intern.svelte';
	import Skills from '$lib/components/skills.svelte';
	import { onMount } from 'svelte';

	let viewportWidth;
	// @ts-ignore
	let width;
	const width_712 = 24;
	const width_1k = 42;

	onMount(() => {
		viewportWidth = window.innerWidth;
		if (viewportWidth > 712) {
			console.log(viewportWidth);
			width = width_1k;
		} else {
			width = width_712;
		}
		window.addEventListener('resize', () => {
			viewportWidth = window.innerWidth;
			if (viewportWidth > 712) {
				console.log(viewportWidth);
				width = width_1k;
			} else {
				width = width_712;
			}
		});
	});
</script>

<div class="app">
	<div class="header">
		<div class="bar">
			<div class="logo">
				<Logo iconColor="#000" />
			</div>
			<div class="name">
				<div class="fname">RISHIKANTH</div>
				<div class="lname">CHANDRASEKARAN</div>
			</div>
		</div>
	</div>

	<div class="front">
		<div class="intro"><Intro /></div>
		<div class="education"><Education /></div>
		<div class="awards"><Awards /></div>
		<div class="intern"><Intern /></div>
		<div class="skills"><Skills /></div>
	</div>
</div>

<style>
	.logo {
		/*width: 48px;*/
		background-color: #ffd000;
		/*background-color: #da702c;*/
		/*padding: 4px 6px 4px 6px;*/
		padding: 8px;
		display: grid;
		margin-bottom: 4px;
		align-items: center;
		justify-content: center;
		border-radius: 6px;
		height: 38px;
		width: 38px;
	}
	.bar {
		display: flex;
		align-items: center;
		gap: 1rem;
		font-size: 20px;
	}
	.name {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		align-items: center;
		gap: 2px;
		font-size: 1.3em;
		color: #100f0f;
		margin: 0;
		padding: 0;
	}
	.fname,
	.lname {
		font-family: Lombok, sans-serif;
		display: flex;
		align-items: flex-start;
		justify-content: center;
		vertical-align: middle;
		text-align: center;
		padding: 0;
		margin: 0;
	}
	.front {
		display: grid;
		align-items: top;
		max-width: 1920px;
		justify-content: center;
		/*grid-auto-columns: 1fr;*/
		gap: 4em;
		margin: 4em auto 0em auto;
	}
	.app {
		height: 98svh;
		margin: 0 auto;
		width: fit-content;
		/*overflow: hidden;*/
	}
	@media (min-width: 710px) {
		.skills {
			grid-area: five;
		}
		.intern {
			grid-area: four;
		}
		.intro {
			grid-area: one;
		}
		.education {
			grid-area: two;
		}
		.awards {
			grid-area: three;
		}
		.front {
			gap: 3em 8em;
			margin-top: 2em;
			width: 90%;
			grid-template-areas:
				'one one'
				'two three'
				'four five';
		}

		.bar {
			font-size: 32px;
		}
		.logo {
			width: 36px;
			height: 36px;
		}
	}

	/*@media (min-width: 1080px) {*/
	/*	.front {*/
	/*		grid-template-areas:*/
	/*			'one one'*/
	/*			'two three'*/
	/*			'four five';*/
	/*		gap: 6em 2em;*/
	/*	}*/
	/*}*/

	@media (min-width: 1280px) {
		.front {
			grid-auto-columns: 1fr;
			gap: 5em 8em;
			margin-top: 6em;
			/*align-items: end;*/
			/*width: fit-content;*/
			grid-template-areas:
				'. two three'
				'one four five';
		}
		.bar {
			font-size: 48px;
		}
		.name {
			/*font-size: 1.7em;*/
			gap: 0.5em;
		}
		.logo {
			margin-bottom: 10px;
			width: 42px;
			height: 42px;
		}
	}
</style>
