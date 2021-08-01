<div class="container">
    <div class="bg-media">
        <video autoplay muted>
            <source src="image-video.mp4" type="video/mp4" />
        </video>
    </div>
</div>

<style lang="scss">
    .container {
        position: relative;

        overflow: hidden;

        display: flex;
        flex-direction: row;
        place-content: center;

        > * {
            flex: 0 0 auto;
        }

        height: 100vh;
    }


    .bg-media {
        position: relative;

        max-width: 1920px;
        height: 100vh;
    }
    
    video {
        display: block;
        width: 100%;
        height: 100%;

        object-fit: cover;
    }
</style>