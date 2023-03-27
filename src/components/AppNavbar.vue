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
        }
    },
}
</script>


<template>
    <nav>
        <div class="container">

            <a href=""><img src="/img/dc-logo.png" alt=""></a>

            <div>
                <ul>
                    <li v-for="link in links"> {{ link }} </li>
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
                cursor: pointer;
                padding: 30px 10px;
                font-size: 12px;
                font-weight: bold;
                text-transform: uppercase;

                &:hover {
                    color: #0282f9;
                    border-bottom: 3px solid #0282f9;
                }
            }
        }
    }

}

#logo {
    
}

</style>