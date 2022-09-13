<footer class="text-light bg-secondary px-2 py-3 ">
	<div>
		responsive-layout {new Date().getFullYear()}

	</div>
	<div>
		<a href="https://github.com/Fabezio/responsive-layout.git" title="main repo">
			code source
		</a>
	</div>
	<div class="bd-brand-item px-2 inverse">
		made with
		<a href="https://getbootstrap.com" title="Bootstrap">
			<img
				src="https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo.svg"
				alt="Bootstrap"
		
				height="32"
				loading="lazy"
				/> 
		</a> and 
		<a href="https://svelte.dev" title="Svelte">
			<img src="https://cdn.icon-icons.com/icons2/2107/PNG/512/file_type_svelte_icon_130137.png" height="32" alt="Svelte">
		</a>
</div>

	<!-- <div>Made with <img src="" alt=""></div> -->
	<div>web responsive with svelte</div>
	<!-- <div>visit <a class="link-item text-warning" href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</div> -->
</footer>

<style>
	footer a {
		font-weight: bold;
		
	}
	footer {
		display: flex;
		/* flex: 1 1 100%; */
		justify-content: center;
		gap: 0.5em;
		flex-direction: column;
		align-items: center;
	}
	@media (orientation: landscape) {
		footer {
			flex-direction: row;
			justify-content: space-evenly;

	}
		
	}
</style>