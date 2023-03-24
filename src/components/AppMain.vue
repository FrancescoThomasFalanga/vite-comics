<script>
export default {
    data() {
        return {
            mainLinks: [
                {
                    image: "/img/buy-comics-digital-comics.png",
                    text: "Digital Comics",
                },
                {
                    image: "/img/buy-comics-merchandise.png",
                    text: "Dc Merchandise",
                },
                {
                    image: "/img/buy-comics-subscriptions.png",
                    text: "Subscription",
                },
                {
                    image: "/img/buy-comics-shop-locator.png",
                    text: "Comic Shop Locator",
                },
                {
                    image: "/img/buy-dc-power-visa.svg",
                    text: "Dc Power Visa",
                },
            ],
        }
    },
}
</script>


<template>
    <main>
        <div class="container">
            <div class="flex" v-for="link in mainLinks">
                <div>
                    <img :src="link.image" alt="">
                </div>
                <div>
                    <span> {{ link.text }} </span>
                </div>
            </div>
        </div>
    </main>
</template>


<style lang="scss" scoped>

main {
    position: relative;
    background-color: #0282f9;
    z-index: 2;

    .container {
        display: flex;
        justify-content: space-around;
        align-items: center;
        gap: 10px;
        margin: 0 auto;
        max-width: 1200px;
        padding: 30px;

        .flex {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            color: white;
            
            img {
                width: 40px;
            }
    
            span {
                text-transform: uppercase;
                font-size: 14px;
            }
        }

        
    }
}

</style>