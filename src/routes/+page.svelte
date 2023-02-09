<main class="main">
	<header class="header">
		<h1 class="sr-only">Georgi Minkov</h1>
		<img src="/logo-name.svg" alt="" class="logo" width="496" height="111" />
		<p class="description">
			software developer based in Sofia. <br />
			<a href="mailto:gmnullptr@gmail.com">contact ✉</a>
		</p>
	</header>

	<div>
		<p class="tagline">
			<span class="capitalized">pressing</span> keys <br /> in the <br />right order
		</p>
	</div>
</main>

<style>
	:root {
		--primary: hsl(220 91% 37%);
		--secondary: hsl(209 97% 88%);
		--initial-bg: var(--secondary);
		--target-bg: hsl(209 97% 91%);
	}

	:global(*) {
		box-sizing: border-box;
		padding: 0;
		margin: 0;
	}

	:gloal(html) {
		animation: reveal-page 1s ease-out 1 forwards;
	}

	@keyframes reveal-page {
		from {
			opacity: 0;
		}
		to {
			opacity: 1;
		}
	}

	:global(body) {
		transition: background-color;
		background-color: var(--initial-bg);
		font-size: 100%;
		animation: reveal-bg 4s ease-in 1 forwards;
	}

	@keyframes reveal-bg {
		from {
			background-color: var(--initial-bg);
		}
		to {
			background-color: var(--target-bg);
		}
	}

	.main {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: flex-start;
		padding: clamp(3rem, calc(1.88rem + 5.63vw), 7.5rem);
		min-height: 100vh;
	}

	a {
		color: inherit;
		text-decoration: none;
	}

	.sr-only {
		position: absolute;
		width: 1px;
		height: 1px;
		padding: 0;
		margin: -1px;
		overflow: hidden;
		clip: rect(0, 0, 0, 0);
		white-space: nowrap;
		border-width: 0;
	}

	.header {
		margin-bottom: 2rem;
		animation: reveal-header 1s ease-out 1 forwards;
	}

	.description {
		color: var(--primary);
		margin-top: 1rem;
		font-size: 2rem;
	}

	@keyframes reveal-header {
		from {
			opacity: 0;
		}
		to {
			opacity: 1;
		}
	}

	.logo {
		max-width: 100%;
		height: auto;
	}

	.tagline {
		font-family: 'Press Start 2P', sans-serif;
		margin: 0;
		line-height: 120%;
		font-size: clamp(2.5rem, calc(1.89rem + 3.03vw), 5rem);
		color: var(--initial-bg);
		animation: reveal-tagline 2s cubic-bezier(0.25, 0.46, 0.45, 0.94) 1 forwards;
		word-break: break-word;
		hyphens: auto;
	}

	@font-face {
		font-family: 'Press Start 2P';
		font-style: normal;
		font-weight: 400;
		font-display: swap;
		src: url(/tagline-font.woff2) format('woff2');
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
