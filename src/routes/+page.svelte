<script>
	import Education from '$lib/components/education.svelte';
	import Awards from '$lib/components/awards.svelte';
	import Intern from '$lib/components/intern.svelte';
	import Skills from '$lib/components/skills.svelte';
</script>

<div class="front">
	<div class="education"><Education /></div>
	<div class="awards"><Awards /></div>
	<div class="intern"><Intern /></div>
	<div class="skills"><Skills /></div>
</div>

<style>
	.front {
		display: grid;
		align-items: top;
		justify-content: center;
		/*overflow-y: scroll;*/
		/*grid-auto-columns: 1fr;*/
		gap: 4em;
		margin: 4em auto 0em auto;
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
	}
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
	}
	@media (min-width: 1920px) {
		.front {
			grid-auto-columns: 1fr;
			gap: 5em 8em;
			grid-template-areas:
				'two three'
				'four five';
		}
	}
</style>
