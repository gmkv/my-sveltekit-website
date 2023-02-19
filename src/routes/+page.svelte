<script>
	import Logo from "$lib/Logo.svelte";
	import GithubIcon from "$lib/GithubIcon.svelte";
	import EmailIcon from "$lib/EmailIcon.svelte";
</script>

<header>
	<Logo />

	<p class="description">software developer based in Sofia</p>
	<ul class="links">
		<li>
			<a href="mailto:gmnullptr@gmail.com"><EmailIcon />contact</a>
		</li>
		<li>
			<a href="https://github.com/gmkv"> <GithubIcon />github</a>
		</li>
	</ul>
</header>

<div>
	<p class="tagline">
		<span class="capitalized">pressing</span> keys<br /> in the <br />right order
	</p>
</div>

<style>
	ul {
		list-style: none;
	}

	a {
		color: inherit;
		text-decoration: none;
	}

	p,
	ul {
		font-family: "Inter", monospace;
		color: var(--primary);
		font-size: 2rem;
	}

	.description,
	.links {
		margin-top: 1rem;
	}

	header {
		margin-bottom: 2rem;
		animation: reveal-header 1s ease-out 1 forwards;
	}

	@keyframes reveal-header {
		from {
			opacity: 0;
		}
		to {
			opacity: 1;
		}
	}

	.tagline {
		line-height: 100%;
		font-size: clamp(2.5rem, calc(1.89rem + 3.03vw), 5rem);
		color: var(--initial-bg);
		animation: reveal-tagline 2s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1 forwards;
		word-break: break-word;
		hyphens: auto;
	}

	@keyframes reveal-tagline {
		from {
			color: var(--initial-bg);
			transform: translateY(-1rem);
		}
		to {
			color: var(--primary);
			transform: translateY(0);
		}
	}

	.capitalized {
		text-transform: capitalize;
	}
</style>
