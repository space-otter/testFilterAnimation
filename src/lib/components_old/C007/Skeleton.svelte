<div class="c007 g-oversize-container">
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
    .c007 {
        background-color: var(--g-clr-gray-001);
        
        padding: 2.5rem 0;

        .start {
            grid-column: 2 / -1;
            overflow: hidden;

            padding: 0 0 2.5rem 0;

            @media only screen and (min-width: 760px) {
                grid-column: 2 / -2;
            }

            @media only screen and (min-width: 1440px) {
                grid-column: 4 / -5;
            }
        }

        .end {
            grid-column: 3 / -3;

            padding: 2.5rem 0 0 0;

            @media only screen and (min-width: 1440px) {
                grid-column: -5 / -3;
                place-self: start;
            }
        }
    }
</style>