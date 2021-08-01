<div class="c010 g-oversize-container">
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
    .c010 {
        background-color: var(--g-clr-gray-002);

        padding: 5rem 0 3.125rem 0;

        .start {
            grid-column: 2 / -2;

            padding-bottom: 3.125rem;

            @media only screen and (min-width: 760px) {
                grid-column: 2 / -4;
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

        @media only screen and (min-width: 760px) {
            padding: 7.5rem 0 2.5rem 0;
        }

        @media only screen and (min-width: 1440px) {
            padding: 9.375rem 0 3.75rem 0;
        }
    }
</style>