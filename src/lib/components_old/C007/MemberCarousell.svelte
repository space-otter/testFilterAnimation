<script>
    import MemberCard from "$lib/components/C007/MemberCard.svelte";

    let members = [
        {
            name: "Torben Andresen",
            position: "Concept Specialist",
            additional: "Co-Founder",
            image: {
                url: "TAN-Shooting-01-Torben.png",
                alt: "",
            },
            address: {
                office: "Büro Hildesheim",
                street: "Osterstraße 21",
                city: "52773 Hildesheim"
            }
        },
        {
            name: "Dominik Fusek",
            position: "UX Specialist",
            additional: "Co-Founder",
            image: {
                url: "DFU-Shooting-03-Dominik.png",
                alt: "",
            },
            address: {
                office: "Büro Köln",
                street: "Thurner Str. 90",
                city: "51069 Köln"
            }
        },
        {
            name: "Luca Rusch",
            position: "Brand Specialist",
            additional: "",
            image: {
                url: "LRU-Shooting-03-Luca.png",
                alt: "",
            },
            address: {
                office: "Büro Köln",
                street: "Thurner Str. 90",
                city: "51069 Köln"
            }
        },
    ]
</script>

<div class="carousell">
    {#each members as member}
        <div>
            <MemberCard
                name={member.name}
                position={member.position}
                additional={member.additional}
                image={member.image}
                address={member.address} />
        </div>
    {/each}
</div>

<style lang="scss">
    .carousell {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;


        overflow-x: scroll;
        -ms-overflow-style: none;  /* IE and Edge */
        scrollbar-width: none;  /* Firefox */

        * {
            flex: 0 0 auto;
            perspective: 500px;

            & + * {
                margin-left: 4rem;

            }

            &:last-child {
                margin-right: 2rem;

                @media only screen and (min-width: 760px) {
                    margin-right: 0;
                }
            }
        }

        ::-webkit-scrollbar {
            display: none;
        }

        @media only screen and (min-width: 760px) {
            overflow-x: visible;
            place-content: center;
        }

        @media only screen and (min-width: 1440px) {
            place-content: start;
        }
    }
</style>