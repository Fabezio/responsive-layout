<script lang="ts" >
	import Header from '$lib/components/layout/Header.svelte';
	import Footer from '$lib/components/layout/Footer.svelte';
	import Navbar from '$lib/components/layout/Navbar/+file.svelte';

	import '../app.css';

	$: innerWidth = 0
	$: innerHeight = 0

	$: landscape = innerWidth > innerHeight
	$: portrait = innerWidth < innerHeight

	let className = "";
	$: if (landscape) className="landcape";
	$: if (portrait) className="portrait";

</script>

<svelte:window bind:innerHeight bind:innerWidth />

<Header>
	<Navbar />
</Header>
<!-- <div class="container"> -->

	<main  class={className}>
		<slot />
	</main>
	
	<Footer />
<!-- </div> -->

<style>
	main {
		flex: 1;
		display: flex;

		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}
	/* .container {
		min-height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	} */
</style>
