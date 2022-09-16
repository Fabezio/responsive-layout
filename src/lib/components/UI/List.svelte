<script lang="ts">
export let list: string[]
</script>
<ul class="list-group" >
    {#each list as item}
    <li class="list-group-item" >
        {item}

    </li>
    {/each}

</ul>
