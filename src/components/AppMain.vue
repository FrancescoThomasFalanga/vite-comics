<script>
export default {
    data() {
        return {
            isClick: null,
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

    methods: {
        myFilter: function(index) {
            this.isClick = index;
        }
    }
}
</script>


<template>
    <main>
        <div class="container">
            <div class="flex" v-for="(link, index) in mainLinks" @click="myFilter(index)" :class="isClick == index ? 'active' : '' ">
                    <img :src="link.image" :alt="'img: ' + index">
                    <span> {{ link.text }} </span>
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
        justify-content: center;
        align-items: center;
        margin: 0 auto;
        max-width: 1200px;
        padding: 0 30px;

        .flex {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            padding: 30px;
            color: white;
            cursor: pointer;

            &:hover {
                background-color: #0265f9;
            }
            
            img {
                width: 40px;
                height: 40px;
                object-fit: contain;
            }
            
            span {
                text-transform: uppercase;
                font-size: 14px;
            }
        }
        .active {
            background-color: #0265f9;
        }

    }
}

</style>