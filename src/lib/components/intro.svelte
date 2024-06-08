<script>
	const intro = `A recent Computer Science PhD graduate from the University of California, San Diego. My thesis proposed methods to improve computational efficiency of deep learning models.
         I'm a proponent of open-source software and an avid self-hoster.`;
</script>

<div class="intro">
	<div class="text"><img src="/rishi.png" alt="photo" class="circly" />{intro}</div>
	<div class="job">
		I'm seeking jobs in Machine Learning/Artificial Intelligence. My latest <a
			target="blank"
			href="/Rishi-CV.pdf">CV</a
		>.
	</div>
	<div class="contact">
		<div class="pre">Connect with me on:</div>
		<div class="email"><a href="mailto:r3chandr@ucsd.edu">email</a></div>
		<div class="git"><a href="https://github.com/rishikanthc">git</a></div>
		<div class="linkedin"><a href="">linkedin</a></div>
	</div>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=ABeeZee:ital@0;1&display=swap');
	.intro {
		/*width: 100%;*/
		/*font-family: ABeeZee, sans-serif;*/
		margin: 0 auto;
		font-size: 16px;
		line-height: 1.5;
		text-align: justify;
		display: flex;
		flex-direction: column;
		gap: 1em;
		height: 100%;
		align-items: end;
		justify-content: end;
	}

	a {
		text-decoration: none;
		color: #205ea6;
	}
	.contact {
		display: flex;
		gap: 0.8em;
		font-size: 0.9em;
		height: fit-content;
	}
	.text {
		margin: 0 auto;
	}
	.circly {
		display: none;
	}
	@media (min-width: 710px) {
		.intro {
			width: 90%;
		}
	}
	@media (min-width: 1280px) {
		.intro {
			align-items: end;
			justify-content: end;
			width: 75%;
		}
		.circly {
			display: block;
			float: left;
			width: 88px;
			height: 88px;
			border-radius: 50%;
			margin: 0.5em;
		}
		.job {
			font-size: 1.2em;
			color: #a02f6f;
		}
		.text p {
			clear: both;
		}
	}
	@media (min-width: 1920px) {
		.intro {
			align-items: end;
			justify-content: end;
			width: 70%;
		}
	}
</style>
