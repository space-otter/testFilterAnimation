<script>
    import { onMount } from "svelte"

    let nojs = true
</script>

<div class="container" class:nojs>
    <div class="main">
        <p class="slogan g-font-primary-bold">
            <span>We create</span>
            <span>experiences</span>
            <span>for the future.</span>
        </p>
        <div class="tag">
        </div>
    </div>    
    <div class="">
        {#if nojs}
            <p>Some more Info</p>
        {/if}
    </div>
</div>
{#if nojs}
    <div class="expanded-info">

    </div>
{/if}

<style lang="scss">
    .main {
        min-height: 100vh;

        background-color: #000000;
        color: #ffffff;

        .slogan {
            display: flex;
            flex-direction: column;
            flex-wrap: nowrap;

            font-size: 2.25rem;

            &::after {
                content: "";
                position: relative;
                display: block;

                height: 0.25rem;
                width: 2ch;

                margin-top: 0.5em;

                background-color: #ffffff;
            }

            & > * {
                flex: 0 1 auto;
            }

            & > span {
                display: inline-block;

                & + span {
                    margin-top: 0.25em;
                }
            }
        }
    }

    p {
        margin: 0;
    }
</style>