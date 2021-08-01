<script>
    import CarousellTile from "$lib/components_old/C005/CarousellTile.svelte";
    import Headline from "$lib/components_old/C005/Headline.svelte";
    import Skeleton from "$lib/components_old/C005/Skeleton.svelte";
</script>

<Skeleton>
    <svelte:fragment slot="start">
        <Headline />
    </svelte:fragment>
    <svelte:fragment slot="end">
        <CarousellTile />
    </svelte:fragment>
</Skeleton>