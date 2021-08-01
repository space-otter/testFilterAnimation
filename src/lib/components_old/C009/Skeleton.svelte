<div class="c009 g-oversize-container">
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
    .c009 {
        background-color: var(--g-clr-gray-001);
        background: linear-gradient(-180deg, var(--g-clr-gray-001) 65%, var(--g-clr-gray-002) 65%);

        .g-comp {
            padding: 5rem 0;

            .start {
                grid-column: 2 / -2;

                padding-bottom: 2.5rem;

                @media only screen and (min-width: 760px) {
                    padding-bottom: 3.75rem;
                }

                @media only screen and (min-width: 1440px) {
                    grid-column: 3 / -3;
                }
            }

            .end {
                grid-column: 2 / -2;

                @media only screen and (min-width: 760px) {

                }

                @media only screen and (min-width: 1440px) {
                    grid-column: 3 / -3;
                }
            }
        }
    }
</style>