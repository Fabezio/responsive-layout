<script lang="ts" >
	import logo from '../svelte-logo.svg';
  import {links }from './links';
  import Linkdata from './Linkdata.svelte';
	import Brand from './Brand.svelte';
	import Dropdown from "./Dropdown.svelte"
	import { page } from '$app/stores';
	$: collapse = true;
	function toggle() {
		collapse = !collapse;
	}
	
</script>

<nav data-sveltekit-prefetch class="navbar navbar-expand-lg navbar-dark bg-secondary">
	<div class="container-fluid">
		<Brand>
			
				<img height="48" src={logo} alt="SvelteKit" />
			<!-- </a> -->
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
					<!-- <li on:click={toggle} class="nav-item" class:active={$page.url.pathname === url}>
						<a href={url} aria-current="page" class="nav-link" class:disabled>{title}</a>
					</li> -->
				{/each}
				<!-- <Dropdown /> -->

				
			</ul>
			<!-- <form class="d-flex" role="search">
				<input class="form-control me-2" type="search" placeholder="Search" aria-label="Search" />
				<button class="btn btn-outline-success" type="submit">Search</button>
			</form> -->
		</div>
	</div>
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
