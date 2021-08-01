<script>
    import CatchPhrase from "$lib/components_old/C003/CatchPhrase.svelte";
    import Image from "$lib/components_old/C003/Image.svelte";
    import LinkList from "$lib/components_old/C003/LinkList.svelte";
    import Skeleton from "$lib/components_old/C003/Skeleton.svelte";
</script>

<Skeleton>
    <svelte:fragment slot="start">
        <CatchPhrase />
    </svelte:fragment>
    <svelte:fragment slot="mid">
        <Image />
    </svelte:fragment>
    <svelte:fragment slot="end">
        <LinkList />
    </svelte:fragment>
</Skeleton>