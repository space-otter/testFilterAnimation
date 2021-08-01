<script>
    import Headline from "$lib/components/C010/Headline.svelte";
    import Services from "$lib/components/C010/Services.svelte";
    import Skeleton from "$lib/components/C010/Skeleton.svelte";
</script>

<Skeleton>
    <svelte:fragment slot="start">
        <Headline />
    </svelte:fragment>
    <svelte:fragment slot="end">
        <Services />
    </svelte:fragment>
</Skeleton>