<script>
    import Headline from "$lib/components_old/C009/Headline.svelte";
    import Carousell from "$lib/components_old/C009/Carousell.svelte";
    import Skeleton from "$lib/components_old/C009/Skeleton.svelte";
</script>

<Skeleton>
    <svelte:fragment slot="start">
        <Headline />
    </svelte:fragment>
    <svelte:fragment slot="end">
        <Carousell />
    </svelte:fragment>
</Skeleton>