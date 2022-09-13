<script lang="ts" >
  import { createEventDispatcher } from "svelte"
  // const dispatch = createEventDispatcher()
  import { page } from '$app/stores';
	$: collapse = true;
	function toggle() {
    collapse = !collapse;
	}
  type Linkdata = {
    url: string,
    title: string,
    disabled: boolean,
  }
  export let linkdata : Linkdata
  const {url, title, disabled } = linkdata

</script>

<li on:click={toggle} class="nav-item" class:active={$page.url.pathname === url}>
	<a  href={url} aria-current="page" class="nav-link text-uppercase" class:disabled={disabled} >{title}</a>
</li>

<style>
  a {
    text-align: center;
  }
  @media (orientation: landscape) {
    a {
      text-align: left;

  }
  }
</style>
