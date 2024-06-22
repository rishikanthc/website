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
			<Logo iconColor="#001141" />
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
		<slot />
	</div>
</div>

<style>
	.logo {
		/*width: 48px;*/
		background-color: #ffd000;
		background-color: #fedc69;
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
		z-index: 500;
		position: fixed;
		width: 100%;
		top: 0;
		left: 0;
		padding: 0.5em;
		background-color: #fff;
		background-color: #161616;
		/*background-color: #fffcf0;*/
	}
	.name {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		align-items: center;
		gap: 2px;
		font-size: 32px;
		/* font-size: 1.3em; */
		color: #100f0f;
		color: #1261fe;
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

	.app {
		width: min(100%, 1920px);
		/* max-width: 1920px; */
		margin: 0 auto;
		/*overflow: hidden;*/
	}
	@media (min-width: 710px) {
		.header {
			font-size: 32px;
		}
		.logo {
			width: 36px;
			height: 36px;
		}
		.name {
			font-size: 48px;
			gap: 0.5em;
		}
	}

	@media (min-width: 1280px) {
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
		.name {
			font-size: 56px;
			gap: 0.5em;
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
		.header {
			font-size: 48px;
		}
		.name {
			/*font-size: 1.7em;*/
			gap: 0.5em;
		}
	}
</style>
