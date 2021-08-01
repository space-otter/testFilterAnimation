<p class="catch-phrase g-font-primary-bold">
    <span>Hello!</span>
    <span>We are</span>
    <span class="highlighted">Team Inno</span>
</p>

<style lang="scss">
    .catch-phrase {
        margin: 0;

        color: var(--g-clr-white);

        font-size: 3.75rem;
        line-height: 1em;

        span {
            display: block;

            text-align: center;

            @media only screen and (min-width: 760px) {
                display: inline-block;

                &:last-child {
                    display: block;
                }
            }

            @media only screen and (min-width: 1440px) {
                display: block;
                
                text-align: end;
            }
        }

        .highlighted {
            color: var(--g-clr-inno-blue);
        }

        @media only screen and (min-width: 760px) {
            font-size: 5rem;
        }

        @media only screen and (min-width: 1440px) {
            font-size: 7.25rem;
        }
    }    
</style>