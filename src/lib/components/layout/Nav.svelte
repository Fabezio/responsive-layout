<script>
	import logo from './svelte-logo.svg';

  import {page} from '$app/stores';
	$: collapse = true
	function toggle() {
		collapse = !collapse
	}
	const links = [
		{url: "/", title: "Home", disabled: false},
		{url: "/about", title: "about", disabled: false},
		{url: "/todos", title: "Todos", disabled: true}
	]

</script>

<nav data-sveltekit-prefetch class="navbar navbar-expand-md navbar-dark bg-secondary">
	<div  class="container-fluid">
		<div class="brand">
			<a  href="https://kit.svelte.dev">
				<img  height="48" src={logo} alt="SvelteKit" />
			</a>

		</div>

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
		<div class:collapse={collapse} class="navbar-collapse " id="navbarSupportedContent">
			<ul class="navbar-nav me-auto mb-2 mb-lg-0 bg-secondary">
				{#each links as {url, title, disabled} }
					<li on:click={toggle} class="nav-item" class:active={$page.url.pathname === url}>
							<a href={url} aria-current="page"
								class="nav-link" class:disabled={disabled} >{title}</a>
					</li>
					
				{/each}

				<!-- <li class="nav-item">
					<a class="nav-link active" aria-current="page" href="#">Home</a>
				</li>
				<li class="nav-item">
					<a class="nav-link" href="#">Link</a>
				</li>
				
				<li class="nav-item">
					<a class="nav-link disabled">Disabled</a>
				</li> -->
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
	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);

	}

	/* svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	} */

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}
	nav a {
		text-transform: uppercase;
	}

	/* li {
		position: relative;
		height: 100%;
	}

	li.active::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--accent-color);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--heading-color);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	} */
  </style>