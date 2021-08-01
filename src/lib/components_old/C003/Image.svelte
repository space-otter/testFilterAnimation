<picture>
    <img src="/c003-image.png" alt="" />
</picture>

<style lang="scss">
    img {
        max-height: 450px;

        animation-name: swing;
        animation-duration: 2.5s;
        animation-direction: alternate;
        animation-fill-mode: forwards;
        animation-iteration-count: infinite;
        animation-timing-function: ease-in-out;
        animation-delay: 0;
        transform-origin: 25% top;

        @media only screen and (min-width: 1440px) {
            max-height: 540px;
        }

        @keyframes swing {
            to {transform: perspective(500px) rotateX(2deg) rotateY(4deg) rotateZ(-5deg);}
            from {transform: perspective(500px) rotateX(-2deg) rotateY(-2deg) rotateZ(5deg);}
        }
    }
</style>