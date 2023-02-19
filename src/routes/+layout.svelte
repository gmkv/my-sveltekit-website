<script lang="ts">
	import "./styles.css";
</script>

<main>
	<slot />
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: flex-start;
		padding: clamp(3rem, calc(1.88rem + 5.63vw), 7.5rem);
		min-height: 100dvh;
	}
</style>
