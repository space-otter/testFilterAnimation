<div class="cta">
    <span class="g-font-primary-bold">Let's Talk</span>
    <a href="/" class="g-font-secondary-regular">
        Zum Kontaktbereich
        <svg xmlns="http://www.w3.org/2000/svg"
            width="24" height="24" viewBox="0 0 24 24"
            fill="none" stroke="currentColor" stroke-width="2"
            stroke-linecap="round" stroke-linejoin="round">
                <line x1="5" y1="12" x2="19" y2="12"></line>
                <polyline points="12 5 19 12 12 19"></polyline>
        </svg>
    </a>
</div>

<style lang="scss">
    .cta {
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;
        place-content: center;
        place-items: center;

        span {
            display: inline-block;

            font-size: 5rem;

            color: var(--g-clr-white);


            @media only screen and (min-width: 760px) {
                font-size: 9.375rem;
            }

            @media only screen and (min-width: 1440px) {
                font-size: 18.75rem;
            }
        }

        a {
            color: var(--g-clr-white);

            font-size: 1.25rem;

            margin-top: 1.563rem;

            svg {
                display: inline-block;
                position: relative;
                top: -0.1em;
                width: 1em;
                height: 1em;

                margin-left: 0.5em;
            }
        }
    }
</style>