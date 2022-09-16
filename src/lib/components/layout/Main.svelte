<script lang="ts">
// export let orientation = "portrait"
</script>

<main class="my-4" >
    <slot />
</main>

<style>
main {
    /* flex: 1; */
    /* display: flex; */

    padding: 1rem;
    width: 100%;
    /* max-width: 1024px; */
    margin: 0;
    /* padding: 0; */
    box-sizing: border-box;
}

@media (min-width: 768px) {}
</style>
