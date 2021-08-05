<script>
    import { onMount } from "svelte"

    // component states
    let nojs = true
    let onLoadAnimation = false

    onMount(() => {
        nojs = false
        onLoadAnimation = true
    })
</script>

<div class="container" class:nojs>
    <div class="main">
        <div class="slogan g-font-primary-bold"
            class:onLoadAnimation>
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
            <div class="underline-box"></div>
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
    .container {
        padding: 5rem;
        background-color: #000000;
    }
    p {
        margin: 0;
    }
    .main {
        --main-bg: #000000;
        --main-fg-color: #ffffff;

        min-height: 100vh;

        background-color: var(--main-bg);
        color: var(--main-fg-color);

        .slogan {
            --slogan-fg-color: var(--main-fg-color);

            display: flex;
            flex-direction: column;
            flex-wrap: nowrap;

            font-size: 2.25rem;

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

                }
            }


            & > span {
                position: relative;
                display: inline-block;
                //border: 2px solid #ffffff;
            }
        }
        .onLoadAnimation .overlay {
                animation: reveal 2s linear 1s alternate forwards;
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

    @keyframes grow {
        from {
            transform: skewX(10deg) translateX(110%) translateZ(0);
        }
        to {
            transform: skewX(0) translateX(0) translateZ(0);
        }
    }
</style>