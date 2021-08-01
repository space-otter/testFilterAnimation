<script>
    import { onMount } from "svelte";

    let svh;
</script>

<svelte:window bind:innerWidth={svh} />

<div class="container">
    <div class="content">
        <p>Smallest Pixel: {svh}</p>
    </div>
</div>

<style lang="scss">
    .container {
        min-height: 100vh;
        width: 100vw;

        background-color: khaki;
    }
</style>