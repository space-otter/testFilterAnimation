<div class="c011 g-oversize-container">
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
    .c011 {
        background-color: var(--g-clr-gray-002);

        padding: 3.75rem 0 4.375rem 0;

        .start {
            grid-column: 2 / -2;

            padding-bottom: 1.875rem;

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
                grid-column: 3 / span 6;
            }
        }

        @media only screen and (min-width: 760px) {
        }

        @media only screen and (min-width: 1440px) {
            padding-bottom: 5.625rem;
        }
    }
</style>