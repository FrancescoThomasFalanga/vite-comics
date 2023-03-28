<script>
export default {
    data() {
        return {
            links: [
                "Character",
                "Comics",
                "Movies",
                "Tv",
                "Games",
                "Collectibles",
                "Videos",
                "Fans",
                "News",
                "Shop",
            ],

            activeIndex: 0,
        }
    },

    methods: {

        changeIndex(newIndex) {

            this.activeIndex = newIndex;

        },

    }
}
</script>


<template>
    <nav>
        <div class="container">

            <a href=""><img src="/img/dc-logo.png" alt=""></a>

            <div>
                <ul>
                    <li v-for="(link, index) in links" @click="changeIndex(index)" :class="activeIndex == index ? 'active' : '' "> {{ link }} </li>
                </ul>
            </div>
            
        </div>
    </nav>
</template>


<style lang="scss" scoped>

nav {
    background-color: white;


    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 0 auto;
        max-width: 1200px;

        a {
            max-height: 60px;
            
            img {
                width: 60px;
            }
        }


        ul {
            display: flex;
            list-style-type: none;

            li {
                position: relative;
                cursor: pointer;
                padding: 30px 10px;
                font-size: 12px;
                font-weight: bold;
                text-transform: uppercase;


                &.active::before {
                    content: "";
                    position: absolute;
                    display: flex;
                    bottom: 0;
                    left: 0;
                    width: 100%;
                    border-bottom: 3px solid #0282f9;
                }

                &:hover {
                    color: #0282f9;
                }
            }
        }
    }

}

</style>