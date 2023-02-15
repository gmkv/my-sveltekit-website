<main class="main">
	<header class="header">
		<h1 class="sr-only">Georgi Minkov</h1>
		<img src="/logo-name.svg" alt="" class="logo" width="496" height="111" />
		<p class="description">
			software developer based in Sofia. <br />
		</p>
		<ul class="links">
			<li><a href="mailto:gmnullptr@gmail.com"><svg role="presentation" class="at" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M13.718 10.528c0 .792-.268 1.829-.684 2.642-1.009 1.98-3.063 1.967-3.063-.14 0-.786.27-1.799.687-2.58 1.021-1.925 3.06-1.624 3.06.078zm10.282 1.472c0 6.627-5.373 12-12 12s-12-5.373-12-12 5.373-12 12-12 12 5.373 12 12zm-5-1.194c0-3.246-2.631-5.601-6.256-5.601-4.967 0-7.744 3.149-7.744 7.073 0 3.672 2.467 6.517 7.024 6.517 2.52 0 4.124-.726 5.122-1.288l-.687-.991c-1.022.593-2.251 1.136-4.256 1.136-3.429 0-5.733-2.199-5.733-5.473 0-5.714 6.401-6.758 9.214-5.071 2.624 1.642 2.524 5.578.582 7.083-1.034.826-2.199.799-1.821-.756 0 0 1.212-4.489 1.354-4.975h-1.364l-.271.952c-.278-.785-.943-1.295-1.911-1.295-2.018 0-3.722 2.19-3.722 4.783 0 1.73.913 2.804 2.38 2.804 1.283 0 1.95-.726 2.364-1.373-.3 2.898 5.725 1.557 5.725-3.525z"/></svg>contact</a></li>
			<li><a href="https://github.com/gmkv"><svg role="presentation" class="gh" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>github</a></li>
		</ul>
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

	:global(html) {
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
		min-height: 100dvh;
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

	.description, .links {
		color: var(--primary);
		margin-top: 1rem;
		font-size: 2rem;
	}

	.links {
		list-style: none;
	}

	.gh, .at { 
		fill: var(--primary);
		height: 2rem;
		width: 2rem;
		margin-right: 0.5rem;
		vertical-align: middle;
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
