<script>
    import C003 from "$lib/components_old/C003.svelte"
    import C005 from "$lib/components_old/C005.svelte"
    import C006 from "$lib/components_old/C006.svelte"
    import C007 from "$lib/components_old/C007.svelte"
    import C008 from "$lib/components_old/C008.svelte"
    import C009 from "$lib/components_old/C009.svelte"
    import C010 from "$lib/components_old/C010.svelte"
    import C012 from "$lib/components_old/C012.svelte"
</script>

<div class="baustelle">Baustelle</div>
<C003 />
<C005 />
<C006 />
<C007 />
<C008 />
<C009 />
<C010 />
<C012 />
<div class="baustelle">Baustelle</div>

<style lang="scss">
    .baustelle {
        display: flex;
        place-items: center;
        place-content: center;
        background-color: burlywood;
        color: black;

        font-size: 30px;

        height: 100vh;
    }
</style>