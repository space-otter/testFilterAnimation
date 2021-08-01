<script>
    import CTA from "$lib/components_old/C007/CTA.svelte";
    import MemberCarousell from "$lib/components_old/C007/MemberCarousell.svelte";
    import Skeleton from "$lib/components_old/C007/Skeleton.svelte";
</script>

<Skeleton>
    <svelte:fragment slot="start">
        <MemberCarousell />
    </svelte:fragment>
    <svelte:fragment slot="end">
        <CTA />
    </svelte:fragment>
</Skeleton>