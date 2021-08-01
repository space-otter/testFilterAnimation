<div class="secondTile g-oversize-container">
    <div class="g-comp g-comp-grid">
            <div class="content">
                <div class="label">
                    <svg xmlns="http://www.w3.org/2000/svg" width="25" height="45" viewBox="0 0 25 45">
                        <g id="Group_4481" data-name="Group 4481" transform="translate(-856 -409)">
                        <g id="Rectangle_4837" data-name="Rectangle 4837" transform="translate(856 409)" fill="none" stroke="#000" stroke-width="3">
                            <rect width="25" height="45" rx="6" stroke="none"/>
                            <rect x="1.5" y="1.5" width="22" height="42" rx="4.5" fill="none"/>
                        </g>
                        <rect id="Rectangle_4838" data-name="Rectangle 4838" width="11" height="5" rx="2" transform="translate(863 409)"/>
                        </g>
                    </svg>
                    <span class="g-font-secondary-regular">UX Konzept</span>              
                </div>
                <p class="g-font-primary-bold">App wird Helfer bei Verständnis von Fatigue</p>
            </div>
        <div class="cta g-font-secondary-regular">
            <button>
                Case Studie
            </button>
        </div>
    </div>
</div>

<style lang="scss">
    .secondTile {
        min-height: 100vh;
    }

    .g-comp {
        grid-template-rows: repeat(3, 1fr);
    }

    .cta {
        grid-column: 2 / -2;
        grid-row: 3 / 4;
        place-self: end center;

        margin-bottom: 2em;

        button {
            display: block;
            margin: 0;
            border: none;

            font-size: 1.25rem;

            padding: 0.5em 1em;

            background-color: var(--g-clr-black);
            color: var(--g-clr-white);
        }
    }

    .content {
            display: flex;
            flex-direction: column;
            place-items: center;

            grid-column: 2 / -2;
            grid-row: 2 / 3;
        span {
            font-size: 1.25rem;
            display: inline-block;
            margin-left: 0.5em;
        }
    }

    p {
        font-size: 2.5rem;
        text-align: center;
    }
</style>