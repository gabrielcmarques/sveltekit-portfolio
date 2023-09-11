<script>
	import { modalOpened } from '$lib/store';
	import FaEnvelope from 'svelte-icons/fa/FaEnvelope.svelte';
	import FaGithub from 'svelte-icons/fa/FaGithub.svelte';
	import FaLinkedin from 'svelte-icons/fa/FaLinkedin.svelte';
</script>

<svelte:head>
	<title>Gianmarco Cavallo - Main page</title>
</svelte:head>
<main>
	<h1>Gabriel de Christo Marques</h1>
	<p>Desenvedor de Software 💻</p>
	<div class="icons">
		<div
			role="button"
			tabindex="0"
			on:keypress={() => {
				modalOpened.set(true);
			}}
			on:click={() => {
				modalOpened.set(true);
			}}
		>
			<div class="icon">
				<FaEnvelope />
			</div>
		</div>

		<a
			href="https://github.com/gabrielcmarques"
			aria-label="GitHub"
			target="_blank"
			rel="noopener noreferrer"
		>
			<div class="icon">
				<FaGithub />
			</div>
		</a>
		<a
			href="https://www.linkedin.com/in/gabriel-christo-marques/"
			aria-label="Linkedin"
			target="_blank"
			rel="noopener noreferrer"
		>
			<div class="icon">
				<FaLinkedin />
			</div>
		</a>
	</div>
</main>

<style>
	a {
		font-weight: 400;
		transition: all .2s;
		outline: 2px solid transparent;
		color: var(--white);
		/* color: white;
		text-decoration: none; */
	}
	main {
		text-align: center;
		padding: 0;
		margin: 0 auto;
		text-align: center;

		/* display: flex;
		flex-direction: column;
		height: calc(100vh - 80px - 88px);
		justify-content: center;
		align-items: center; */
	}



	/* p {
	font-size: 2.5rem;
	font-family: 'Jost', sans-serif;
	margin: 1.5rem 0 3.5rem;
	max-width: 700px;
	} */

	/* main > h1 {		
		margin: 50px 10px 0;		
		line-height: 1;
		font-weight: 400;
	} */

	.icons {
		display: flex !important;
		justify-content: center !important;
		align-items: center;
		gap: 20px;
		cursor: pointer;
		font-size: 30px;
		display: flex;
		justify-content: space-between;
		max-width: 200px;
		margin: 50px auto 0;
	}

	.icon {
		cursor: pointer;
		transition: color 0.2s ease-in-out;
		width: 40px;
	}
	.icon:hover {
		color: #ca3c25;
	}

	@media (min-width: 900px) {
		main > h1 {
			font-size: 48px;
		}
	}

	@media (min-width: 600px) {
		main {
			max-width: none;
		}
	}


</style>
