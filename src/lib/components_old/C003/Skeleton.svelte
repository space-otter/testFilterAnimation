<script>
    import { onMount } from "svelte";

    let container;
    let inView = false;

    onMount(() => {
        let opt = {
            threshold: 0.25
        }

        let callback = (entries, observer) => {
            entries.forEach(entry => {
                if(entry.isIntersecting) {
                    inView = true;      
                }
            });
        }

        let observer = new IntersectionObserver(callback, opt);

        observer.observe(container);
    })
</script>

<div class="c003 g-oversize-container" bind:this={container}>
    <section class="g-comp g-comp-grid" class:inView>
        <div class="g-comp-subgrid">
            <div class="start">
                <slot name="start" />
            </div>
            <div class="mid">
                <slot name="mid" />
            </div>
            <div class="end">
                <slot name="end" />
            </div>
        </div>
    </section>
</div>

<style lang="scss">
    .c003 {
        background-color: var(--g-clr-gray-001);

        overflow: hidden;

        & .g-comp {
            padding: 4.375rem 0 5rem 0;

            background-color: var(--g-clr-gray-001);

            & .g-comp-subgrid {
                grid-column: 2 / -2;

                grid-template-columns: repeat(var(--g-comp-grid-cols), 1fr);
                place-items: center center;

                background-color: #D2FAE6;

                & .start {
                    grid-column: 1 / -1;                    

                    padding: 2.5rem 0.625rem 0 0.625rem;

                    @media only screen and (min-width: 1440px) {
                        grid-column: 1 / 6;
                        grid-row: 1 / 2;
                        padding: 0.625rem 0;
                    }
                }

                & .mid {
                    grid-column: 1 / -1;                    

                    @media only screen and (min-width: 1440px) {
                        grid-column: 5 / 11;
                        grid-row: 1 / 2;
                    }
                }

                & .end {
                    grid-column: 1 / -1;
                    z-index: 3;                 

                    padding: 0 0.625rem 2.5rem 0.625rem;

                    @media only screen and (min-width: 1440px) {
                        grid-column: 10 / 13;
                        grid-row: 1 / 2;
                        place-self: center center;

                        padding: 0.625rem 0;
                    }
                }
            }

            &:not(.inView) {
                opacity: 0;
                transition: opacity 2s;
            }

            &.inView {
                opacity: 1;
                transition: opacity 2s;
            }

            @media only screen and (min-width: 760px) {
                padding: 5rem 0 6.25rem 0;
            }

            @media only screen and (min-width: 1440px) {
                padding: 12.5rem 0 11.25rem 0;
            }
        }
    }
</style>