<script>
    let itemBgUrl = "url(c012-image-02.jpg)";
    let containerBgUrl = "url(c012-blur-02.png)";
</script>

<div 
    class="c012 g-fullscale-container"
    style="
        --item-bg: {itemBgUrl};
        --container-bg: {containerBgUrl};">
    <section>
        <div class="item">
            <slot name="item"/>
        </div>
    </section>
</div>

<style lang="scss">
    .c012 {
        background-image: var(--container-bg);
        background-size: cover;

        section {
            display: flex;
            flex-direction: row;
            flex-wrap: nowrap;
            place-content: center;
            place-items: center;

            min-height: 450px;

            background-image: var(--item-bg);
            background-size: cover;
            background-position: center;

            & > * {
                flex: 0 0 auto;
            }

            @media only screen and (min-width: 760px) {
                min-height: 700px;
            }

            @media only screen and (min-width: 1920px) {
                min-height: 900px;
            }
        }
    }
</style>