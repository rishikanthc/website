<script>
	import Logo from '$lib/icons/logo.svelte';
	import Intro from '$lib/components/intro.svelte';
	import Education from '$lib/components/education.svelte';
	import Awards from '$lib/components/awards.svelte';
	import Intern from '$lib/components/intern.svelte';
	import Skills from '$lib/components/skills.svelte';
	import { onMount } from 'svelte';
	import Nav from '$lib/components/nav.svelte';

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
		<div class="logo">
			<Logo iconColor="#000" />
		</div>
		<div class="name">
			<div class="fname">RISHIKANTH</div>
			<div class="lname">CHANDRASEKARAN</div>
		</div>
		<Nav />
	</div>

	<div class="pane">
		<div class="left">
			<div class="intro"><Intro /></div>
		</div>
		<div class="front">
			<div class="education"><Education /></div>
			<div class="awards"><Awards /></div>
			<div class="intern"><Intern /></div>
			<div class="skills"><Skills /></div>
		</div>
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
	.header {
		display: flex;
		align-items: center;
		gap: 1rem;
		font-size: 20px;
		height: 64px;
		z-index: 100;
		position: fixed;
		width: 100%;
		top: 0;
		left: 0;
		padding: 0.5em;
		background-color: #fffcf0;
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
	.pane {
		width: fit-content;
		margin-top: 96px;
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
		justify-content: center;
		/*overflow-y: scroll;*/
		/*grid-auto-columns: 1fr;*/
		gap: 4em;
		margin: 4em auto 0em auto;
	}
	.app {
		max-width: 1920px;
		margin: 0 auto;
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
			/*width: 90%;*/
			grid-template-areas:
				'one one'
				'two three'
				'four five';
		}

		.header {
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
			/*grid-auto-columns: 1fr;*/
			gap: 5em 8em;
			flex: 1;
			/*margin-top: 6em;*/
			/*align-items: end;*/
			/*width: fit-content;*/
			margin-left: 35%;
			height: 100%;
			/*height: calc(100% - 80px);*/
			grid-template-areas:
				'two three'
				'four five';
		}
		.header {
			font-size: 40px;
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
		.header {
			height: 50px;
		}
		.pane {
			display: flex;
			width: 100%;
			margin-top: 150px;
			/*height: calc(100svh - 150px);*/
			justify-content: space-between;
		}
		.left {
			position: fixed;
			bottom: 25px;
			left: 0;
			display: grid;
			align-items: end;
			width: 30%;
		}
	}
	@media (min-width: 1920px) {
		.front {
			grid-auto-columns: 1fr;
			gap: 5em 8em;
			/*margin-top: 6em;*/
			/*align-items: end;*/
			/*width: fit-content;*/
			grid-template-areas:
				'two three'
				'four five';
		}
		.header {
			font-size: 48px;
		}
		.name {
			/*font-size: 1.7em;*/
			gap: 0.5em;
		}
	}
</style>
