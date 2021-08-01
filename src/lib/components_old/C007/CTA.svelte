<a href="/" class="g-font-primary-bold">
    meet the team
    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"
        viewBox="0 0 24 24" fill="none" stroke="currentColor"
        stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
            <line x1="5" y1="12" x2="19" y2="12"></line>
            <polyline points="12 5 19 12 12 19"></polyline>
    </svg>
</a>

<style lang="scss">
    a {
        display: flex;
        flex-direction: column;
        place-items: center;
        color: var(--g-clr-inno-green);

        font-size: 4.375rem;
        line-height: 1.2em;
        text-align: center;
        word-break: keep-all;

        svg {
            position: relative;
            color: var(--g-clr-black);

            display: block;
            width: 0.75em;
            height: 0.75em;

            margin-top: 0.5em;

            @media only screen and (min-width: 760px) {
                top: 0.1em;
                margin-top: 0;
                margin-left: 0.3em;
            }

            @media only screen and (min-width: 1440px) {
                top: 0;
                margin-top: 0.5em;
                margin-left: 0;
            }
        }

        @media only screen and (min-width: 760px) {
            flex-direction: row;
            place-content: center;
        }

        @media only screen and (min-width: 1440px) {
            flex-direction: column;
        }
    }
</style>