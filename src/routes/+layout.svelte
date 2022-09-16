<script lang="ts">
import Header from '$lib/components/layout/Header.svelte';
import Main from '$lib/components/layout/Main.svelte';
import Side from '$lib/components/layout/Side.svelte';
import Footer from '$lib/components/layout/Footer.svelte';
import Navbar from '$lib/components/layout/Navbar/+file.svelte';

import '../app.css';

$: background = "secondary" 
$: theme = "light"


$: innerWidth = 0
$: innerHeight = 0

$: landscape = innerWidth > innerHeight
$: portrait = innerWidth < innerHeight

$: orientation = "";
// $: if (landscape) orientation = "landcape";
$: if (portrait) orientation = "portrait";
</script>

<svelte:window bind:innerHeight bind:innerWidth />

<Header>
    <Navbar {background} {theme} />
</Header>
<!-- <div class="container"> -->
<div class="{orientation} flex-1" >
    <!-- <Side list={["1", "2"]} /> -->
    <Main >
        <slot />
        
    </Main>
    <!-- <Side list={["fabezio", "lolo", "naomie"]} /> -->

</div>
<!-- <main  class={className}>
</main> -->

<Footer {background} {theme} />
<!-- </div> -->

<style>
    .flex-1 {
        display: flex;
        flex: 1;
    }
/* main {

flex: 1;

display: flex;

padding: 1rem;

width: 100%;

max-width: 1024px;

margin: 0 auto;

box-sizing: border-box;
	} */
/* .container {

min-height: 100vh;

display: flex;

flex-direction: column;

justify-content: space-between;
	} */
</style>
