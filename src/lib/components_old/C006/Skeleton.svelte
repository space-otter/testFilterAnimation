<div class="c006 g-oversize-container">
    <section class="g-comp g-comp-grid">
        <div class="start">
            <slot name="start" />
        </div>
        <div class="end">
            <slot name="end" />
        </div>
        <div class="end-side">
            <slot name="end-side" />
        </div>
    </section>
</div>

<style lang="scss">
    .c006 {
        background-color: var(--g-clr-gray-001);

        .g-comp {
            padding-bottom: 1.563rem;

            .start {
                padding: 2.5rem 0 1.25rem 0;
                grid-column: 2 / -2;
                grid-row: 1 / 2;

                @media only screen and (min-width: 760px) {
                    grid-column: 2 / -4;
                }

                @media only screen and (min-width: 1440px) {
                    grid-column: 4 / -7;
                }
            }

            .end {
                grid-column: 2 / -2;
                grid-row: 2 / 3;

                @media only screen and (min-width: 760px) {
                    grid-column: 2 / -5;
                }

                @media only screen and (min-width: 1440px) {
                    grid-column: 4 / span 6;
                }
            }

            .end-side {
                grid-column: 2 / -2;
                place-self: start end;
                
                padding-top: 2.5rem;

                @media only screen and (min-width: 760px) {
                    grid-column: -4 / -2;
                    grid-row: 2 / 3;
                    
                    padding-top: 0;
                }

                @media only screen and (min-width: 1440px) {
                    grid-column: -6 / span 3;
                    grid-row: 2 / 3;
                }
            }

            @media only screen and (min-width: 760px) {
                padding-bottom: 2.188rem;
            }

            @media only screen and (min-width: 1920px) {
                padding-bottom: 3.75rem;
            }
        }
    }    
</style>
