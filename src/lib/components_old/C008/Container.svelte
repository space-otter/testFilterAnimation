<div class="c008 g-oversize-container">
    <section class="g-comp g-comp-grid">
        <div class="item">
            <slot name="item"/>
        </div>
    </section>
    <div class="bg-media">
        <video muted autoplay loop>
            <source src="/cologne.mp4" type="video/mp4" />
        </video>
    </div>
</div>

<style lang="scss">
    .c008 {
        position: relative;

        section {

            position: relative;
            z-index: 2;

            min-height: 700px;

            .g-comp {
                position: relative;
            }

            .item {
                grid-column: 2 / -3;
                place-self: center center;
            }

            padding: 3.75rem 0 7.5rem 0;

            @media only screen and (min-width: 760px) {
                min-height: 700px;

                padding: 6.25rem 0 11.25rem 0;

                .item {
                    grid-column: 2 / -3;
                }
            }

            @media only screen and (min-width: 1440px) {
                min-height: 900px;
                
                padding: 12.5rem 0 13.125em 0;
                
                .item {
                    grid-column: 3 / -3;
                }
            }
        }

        .bg-media {
            position: absolute;
            z-index: 1;

            top: 0;
            left: 0;

            height: 100%;
            width: 100%;

        }

        video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
</style>