<script>
    import { onMount } from "svelte";

    let actualScrollYPos = 0;
    let prevScrollYPos = 0;

    let state = false;
    let first;

    const setScrollYPosIndicator = () => {
        prevScrollYPos = actualScrollYPos;
    }

    const scrollYDirection = () => {
        if (prevScrollYPos > actualScrollYPos) {
            return "up";
        }
        else {
            return "down";
        }
    }

    const morph = (el, direction) => {
        let ctr = 5;

        if (direction === "down") {
            el.style.width = el.clientWidth + ctr + "px";
        }
        else {
            el.style.width = el.clientWidth - ctr + "px";
        }
    }

    onMount(() => {
        let options = {
            threshold: 0
        }

        let callback = (entries, observer) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    window.addEventListener('scroll', () => {
                        morph(first, scrollYDirection());
                        setScrollYPosIndicator();
                    });
                    console.log("running")
                }
                console.log(entry);
            })
        }

        let observer = new IntersectionObserver(callback, options);

        observer.observe(first)
    })
</script>


<div class="container">
    <div class="first"
        bind:this={first}
        >I get red</div>
    <div class="second"></div>
</div>

<svelte:window  bind:scrollY={actualScrollYPos}/>

<style lang="scss">
    .container {
        display: flex;
        flex-direction: column;
        place-items: center;
        min-height: 100vh;

        outline: red 2px solid;

        background-color: var(--g-clr-gray-001);

        & > * {
            flex: 0 0 auto;
        }

        .first {
            display: flex;
            flex-direction: column;
            place-items: center;
            place-content: space-evenly;

            position: relative;
            width: 80%;
            min-width: 80%;
            max-width: 100%;
            height: 100vh;

            margin-top: 200px;

            background-color: #8C9DAC;

            &:not(.grow) {
                transform: scaleX(1);
                transition: transform 2s;
            }
            
            &.grow {
                transform: scaleX(1.2);
                transition: transform 2s;
            }
        }


        .second {
            display: flex;
            flex-direction: column;
            place-items: center;
            place-content: space-evenly;

            height: 100vh;
            width: 100%;

            margin-bottom: calc(100vh * 0.25);
            
            background-color: #00132F;
        }
    }
</style>