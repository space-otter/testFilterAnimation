<script>
    import { onMount } from "svelte"

    let nojs = true

    onMount(() => {
        nojs = false
    })
</script>

<div class="container" class:nojs>
    <div class="main">
        <div class="slogan g-font-primary-bold">
            <div class="overlay-wrapper">
                <div class="overlay"></div>
                <span>We create</span>
            </div>
            <div class="overlay-wrapper">
                <div class="overlay"></div>
                <span>experiences</span>
            </div>
            <div class="overlay-wrapper">
                <div class="overlay"></div>
                <span>for the future.</span>
            </div>
        </div>
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
    p {
        margin: 0;
    }
    .main {
        --container-bg: #000000;
        --main-fg-color: #ffffff;

        min-height: 100vh;

        background-color: var(--container-bg);
        color: var(--main-fg-color);

        .slogan {
            --slogan-fg-color: var(--main-fg-color);

            display: flex;
            flex-direction: column;
            flex-wrap: nowrap;

            font-size: 2.25rem;

            &::after {
                content: "";
                position: relative;
                display: block;

                height: 0.35rem;
                width: 2ch;

                margin-top: 0.5em;

                background-color: var(--slogan-fg-color);
            }

            & > * {
                flex: 0 1 auto;
            }

            & > .overlay-wrapper {
                position: relative;
                display: block;
                
                width: max-content;
                overflow: hidden;
                & + .overlay-wrapper {
                    margin-top: 0.25em;
                }

                & > .overlay {
                    position: absolute;

                    width: 100%;
                    height: 100%;

                    background-color: var(--slogan-fg-color);

                    transform: skewX(0) translateX(0) translateZ(0);

                    animation: reveal 2s linear 0s 1 alternate forwards;
                }
            }

            & > span {
                position: relative;
                display: inline-block;
                //border: 2px solid #ffffff;
            }
        }
    }

    @keyframes reveal {
        from {
            transform: skewX(0) translateX(0) translateZ(0);
        }
        to {
            transform: skewX(20deg) translateX(-110%) translateZ(0);
        }
    }
</style>