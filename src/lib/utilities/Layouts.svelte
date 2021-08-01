<style lang="scss" global>
    .g-oversize-container {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        place-content: center;

        & > * {
            flex: 1 1 auto;
        }

        & > .g-comp {
            @media only screen and (min-width: 320px) {
                max-width: calc(320px + ((760px - 320px) / 2));
            }

            @media only screen and (min-width: 760px) {
                max-width: calc(760px + ((1440px - 760px) / 2));
            }

            @media only screen and (min-width: 1440px) {
                max-width: calc(1440px + ((1920px - 1440px) / 2));
            }

            @media only screen and (min-width: 1920px) {
                max-width: 1920px;
            }
        }
    }

    .g-fullscale-container {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        place-content: center;

        & > * {
            flex: 1 1 auto;
            max-width: 1920px;
        }
    }

    .g-comp {
        &.g-comp-grid {
            --g-comp-grid-cols: 4;
            --g-comp-grid-col-gap: 0.625rem;
            --g-comp-grid-col-spacing: 1.25rem;

            display: grid;
            grid-template-columns:
                calc(var(--g-comp-grid-col-spacing) - var(--g-comp-grid-col-gap))
                repeat(var(--g-comp-grid-cols), 1fr)
                calc(var(--g-comp-grid-col-spacing) - var(--g-comp-grid-col-gap));
            grid-auto-rows: auto;
            column-gap: var(--g-comp-grid-col-gap);

            @media only screen and (min-width: 760px) {
                --g-comp-grid-cols: 8;
                --g-comp-grid-col-spacing: 1.563rem;
            }

            @media only screen and (min-width: 1440px) {
                --g-comp-grid-cols: 12;
                --g-comp-grid-col-spacing: 2.5rem;
            }

            @media only screen and (min-width: 1920px) {
                --g-comp-grid-col-gap: 1rem;
                --g-comp-grid-col-spacing: 8.75rem;
            }

            & > * {
                grid-column: 1 / -1;
            }

            & > .g-comp-subgrid {
                display: grid;
                grid-auto-rows: auto;
                column-gap: var(--g-comp-grid-col-gap);
            }
        }
    }
</style>
