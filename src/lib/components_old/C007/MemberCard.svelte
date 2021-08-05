<script>
    let additional = "";
    let name = "Torben Andresen";
    let position = "Concept Specialist";
    let image = {
        url: "/TAN-Shooting-01-Torben.png",
        alt: ""
    }
    let address = {
        office: "Büro Hildesheim",
        street: "Osterstraße 21",
        city: "52773 Hildesheim"
    }

    let hovering = false;
    
    export { address, additional, image, name, position }
</script>

<div class="container" class:mouseover={hovering}
    on:mouseover={() => hovering = true}
    on:mouseout={() => hovering = false}
    >
    <div class="person">
        <span class="name g-font-primary-bold">{name}</span>
        <span class="position g-font-primary-regular">{position}</span>
        <span class="additional g-font-secondary-regular">{additional}</span>
    </div>
    <div class="image-container">
        <img src={image.url} alt={image.alt} />
    </div>
    <div class="location">
        <svg xmlns="http://www.w3.org/2000/svg"
            width="20" height="20" viewBox="0 0 24 24"
            fill="none" stroke="currentColor" stroke-width="2"
            stroke-linecap="round" stroke-linejoin="round">
                <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path>
                <circle cx="12" cy="10" r="3"></circle>
            </svg>

        <address class="g-font-secondary-regular">
            <span>{address.office}</span>
            <span>{address.street}</span>
            <span>{address.city}</span>
        </address>
    </div>
</div>

<style lang="scss">
    .container{
        @media (hover: hover) {
            transform-origin: 50% 50%;

            &:hover {
                transform: rotateY(10deg) translateX(0.5em);
                opacity: 0.85;
                transition: opacity 200ms 200ms;
                transition: transform 200ms 200ms, opacity 200ms 200ms;
            }

            &:not(:hover) {
                transform: rotateY(0) translateX(0);
                opacity: 1;
                transition: transform 300ms 200ms, opacity 300ms 200ms;
            }
        }
    }

    .person {
        display: flex;
        flex-direction: column;

        span {
            display: inline-block;
            height: 1.2em;
        }

        .name {
            font-size: 1.625rem;
            line-height: 1.2em;

            @media only screen and (min-width: 1440px) {
                font-size: 1.875rem;
            }
        }

        .position {
            font-size: 1.625rem;
            line-height: 1.2em;

            color: var(--g-clr-inno-blue);

            @media only screen and (min-width: 1440px) {
                font-size: 1.875rem;
            }
        }

        .additional {
            font-size: 1.25rem;
            line-height: 1.2em;
        }

        > * + * {
            margin-top: 0.2em;
        }
    }

    .image-container {
        position: relative;
        overflow: hidden;
        margin: 1.563rem 0;

        &::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;

            height: 10rem;
            width: 10rem;

            background-color: var(--g-clr-inno-blue);

            opacity: 0;

            @media (hover: hover) {
                .container:not(.mouseover) & {
                    opacity: 0;
                    transition: opacity 200ms 200ms;
                }

                .container.mouseover & {
                    opacity: 0.25;
                    transition: opacity 200ms 200ms;
                }
            }
        }

        img {
            display: block;
            width: 10rem;
            height: 10rem;

            object-fit: cover;

            background-color: var(--g-clr-gray-002);
        }
    }


    .location {
        address {
            display: flex;
            flex-direction: column;

            font-size: 1.25rem;
            font-style: normal;
        }
    }
</style>