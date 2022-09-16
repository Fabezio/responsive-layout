<script lang="ts">
import List from "$lib/components/UI/List.svelte"
export let list: string[]
// export let side="left"
</script>
<aside >
    <List {list} />
    <!-- <slot />
    </List> -->
</aside>

<style>
aside {
  min-height: 100%;
  min-width: 160px;
  background: transparent;
}
</style>
