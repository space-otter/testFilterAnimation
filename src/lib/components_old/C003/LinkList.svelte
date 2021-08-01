<script>
    let linkList = [
        {title: "Case Studies", url: "/", highlighted: false},
        {title: "Unser Team", url: "/", highlighted: true},
        {title: "Blog", url: "/", highlighted: false},
        {title: "Kontakt", url: "/", highlighted: false},
    ]
</script>

<ul class="g-font-primary-bold">
    {#each linkList as link}
        <li>
            <a href={link.url} class:highlighted={link.highlighted}>
                {link.title}
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"
                    viewBox="0 0 24 24" fill="none" stroke="currentColor"
                    stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                        <line x1="5" y1="12" x2="19" y2="12"></line>
                        <polyline points="12 5 19 12 12 19"></polyline>
                </svg>
            </a>
        </li>
    {/each}
</ul>

<style lang="scss">
    ul {
        margin: 0;
        padding: 0;

        list-style: none;

        font-size: 1.875rem;

        & li {
            a {
                color: var(--g-clr-black);

                &.highlighted {
                    color: var(--g-clr-inno-blue);
                }

                & > svg {
                    display: inline-block;

                    width: 0.85em;
                    height: 0.85em;
                }
            }

            & + li {
                margin-top: 0.65em;

                @media only screen and (min-width: 760px) {
                    margin-top: 0;
                }

                @media only screen and (min-width: 1440px) {
                    margin-top: 0.65em;
                }
            }
        }

        @media only screen and (min-width: 760px) {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            column-gap: 1.5em;
            row-gap: 0.5em;

            font-size: 2.5rem;
        }

        @media only screen and (min-width: 1440px) {
            display: block;
        }
    }
</style>