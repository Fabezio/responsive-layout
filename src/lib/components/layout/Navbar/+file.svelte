<script lang="ts">
    export let background = ""
    export let theme = ""
import logo from '../svelte-logo.svg';
import {
    links
} from './links';
import Linkdata from './Linkdata.svelte';
import Brand from './Brand.svelte';
import Dropdown from "./Dropdown.svelte"
import {
    page
} from '$app/stores';
$: collapse = true;

function toggle() {
    collapse = !collapse;
}
</script>

<!-- <nav data-sveltekit-prefetch class="text-center"> -->
<nav data-sveltekit-prefetch class="justify-content-center navbar navbar-expand-lg navbar-{theme} bg-{background}">
        <h1 class="text-light">Navbar</h1>
        <!-- 
    <div class="container-fluid">
        <Brand>
            <a>
        <img height="48" src={logo} alt="SvelteKit" />
        </a>
        </Brand>

        <button
            class="navbar-toggler"
            on:click={toggle}
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent"
            aria-expanded="false"
            aria-label="Toggle navigation"
            >
            <span class="navbar-toggler-icon" />
        </button>
        <div class:collapse class="navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0 bg-secondary justify-content-end">
                {#each links as linkdata}
                <Linkdata {linkdata}/>
               
                {/each}
                <Dropdown />

            </ul>
            <form class="d-flex" role="search">

<input class="form-control me-2" type="search" placeholder="Search" aria-label="Search" />

<button class="btn btn-outline-success" type="submit">Search</button>
            </form>
        </div>
    </div> -->
</nav>

<!-- <nav data-sveltekit-prefetch class="nav navbar navbar-expand-md">

<div class="brand">

</div>

<ul>

<li class:active={$page.url.pathname === '/'}>

<a href="/">Home</a>

</li>

<li class:active={$page.url.pathname === '/about'}>

<a href="/about">About</a>

</li>

</ul>

</nav> -->

<style>
nav a {
    text-transform: uppercase;
}
</style>
