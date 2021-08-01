<div class="c005 g-oversize-container">
    <section class="g-comp g-comp-grid">
        <div class="start">
            <slot name="start" />
        </div>
        <div class="end">
            <slot name="end" />
        </div>
    </section>
</div>

<style lang="scss">
    .c005 {
        background-color: var(--g-clr-gray-001);

        .g-comp {
            .start {
                padding: 5rem 0 2.5rem 0;
                grid-column: 2 / -2;

                @media only screen and (min-width: 760px) {
                    padding: 6.25rem 0 3.75rem 0; 
                }

                @media only screen and (min-width: 1440px) {
                    grid-column: 3 / -3;

                    padding: 11.25rem 0 3.75rem 0; 
                }
            }

            .end {
                grid-column: 2 / -2;
                padding: 0 0 2.5rem 0;

                @media only screen and (min-width: 1440px) {
                    grid-column: 3 / -3;
                }
            }
        }
    }
</style>