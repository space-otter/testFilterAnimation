<script>
    import Headline from "$lib/components_old/C006/Headline.svelte";
    import SideInfo from "$lib/components_old/C006/SideInfo.svelte";
    import Skeleton from "$lib/components_old/C006/Skeleton.svelte";
    import TextBody from "$lib/components_old/C006/TextBody.svelte";
</script>

<Skeleton>
    <svelte:fragment slot="start">
        <Headline />
    </svelte:fragment>
    <svelte:fragment slot="end">
        <TextBody />
    </svelte:fragment>
    <svelte:fragment slot="end-side">
        <SideInfo />
    </svelte:fragment>
</Skeleton>