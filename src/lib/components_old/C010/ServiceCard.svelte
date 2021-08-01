<script>
    let title = "Konzeption";
    let description = "Nutzerführung und durchdachte Lösungen";
    let active = false;

    export { active, title, description }
</script>

<div
    class="service"
    class:active
    on:mouseover={() => active = true}
    on:mouseleave={() => active = false}>
    <div class="icon-container">
        <slot name="icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="61" height="57" viewBox="0 0 61 57">
            <g id="Group_2365" data-name="Group 2365" transform="translate(-376 -9452)">
                <circle id="Ellipse_800" data-name="Ellipse 800" cx="16" cy="16" r="16" transform="translate(376 9477)" fill="#6aedac"/>
                <g id="Icon" transform="translate(380 9452.026)">
                <rect id="Area" width="57" height="57" transform="translate(0 -0.026)" fill="#fcfcfc" opacity="0"/>
                <g id="Icon-2" data-name="Icon" transform="translate(3.673 7.118)">
                    <circle id="Path" cx="7.125" cy="7.125" r="7.125" transform="translate(17.702 -2.368)" fill="none" stroke="#3d3d3d" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"/>
                    <line id="Line" y1="33.25" transform="translate(24.827 11.882)" fill="none" stroke="#3d3d3d" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"/>
                    <path id="Path-2" data-name="Path" d="M11.875,28.5H4.75a23.75,23.75,0,0,0,47.5,0H45.125" transform="translate(-3.673 -7.118)" fill="none" stroke="#3d3d3d" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"/>
                </g>
                </g>
            </g>
            </svg>
        </slot>
    </div>
    <span class="g-font-primary-bold">{title}</span>
    <p class="g-font-secondary-regular">{description}</p>
</div>

<style lang="scss">
    .service {
        display: flex;
        flex-direction: column;
        place-items: center;
        place-content: center;

        padding: 1.25rem;

        border-radius: 0.5rem;

        background-color: var(--g-clr-white);

        span {
            font-size: 1.125rem;

            text-align: center;

            margin: 0.5em 0 0 0;

            @media only screen and (min-width: 1440px) {
                font-size: 1.5rem;
            }
        }

        &:not(.active) span {
            color: var(--g-clr-black);
            transition: color 200ms 200ms;
        }

        &.active span {
            color: var(--g-clr-white);
            transition: color 200ms 200ms;
        }

        p {
            color: var(--g-clr-gray-003);

            text-align: center;
            
            margin: 0.5em 0 0 0;

            font-size: 0.813rem;

            @media only screen and (min-width: 1440px) {
                font-size: 1rem;
            }
        }

        &:not(.active) p {
            color: var(--g-clr-gray-003);
            transition: color 200ms 200ms;
        }

        &.active p {
            color: var(--g-clr-white);
            transition: color 200ms 200ms;
        }

        @media (hover: hover) {
            &:not(:hover) {
                background-color: var(--g-clr-white);
                transition: background-color 200ms 200ms;
            }

            &:hover {
                background-color: var(--icon-color, var(--g-clr-inno-blue));
                transition: background-color 200ms 200ms;
            }
        }
    }
</style>