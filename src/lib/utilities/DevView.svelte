<script>
    export let name = "";
</script>

<div class="container">
    <h2 class="g-font-primary-bold">{name}</h2>
    <a class="g-font-primary-bold" href="/dev">Go back</a>
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

        a {
            display: block;
            padding: 1em 0;
            color: #ffffff;
        }

        .component {
            border: 2px solid #6AEDAC;
        }
    }
</style>