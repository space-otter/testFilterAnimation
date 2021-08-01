<script>
    export let name = "";
</script>

<div class="container">
    <h2 class="g-font-primary-bold">{name}</h2>
    <div class="component">
        <slot />
    </div>
</div>

<style lang="scss">
    .container {
        min-height: 100vh;

        background-color: #1F2138;
        padding: 2rem;

        h2 {
            color: #ffffff;
        }

        .component {
            border: 2px solid #6AEDAC;
        }
    }
</style>