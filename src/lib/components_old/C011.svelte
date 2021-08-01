<script>
    import Headline from "$lib/components_old/C011/Headline.svelte";
    import Skeleton from "$lib/components_old/C011/Skeleton.svelte";
    import Text from "$lib/components_old/C011/Text.svelte";
</script>

<Skeleton>
    <svelte:fragment slot="start">
        <Headline />
    </svelte:fragment>
    <svelte:fragment slot="end">
        <Text />
    </svelte:fragment>
</Skeleton>