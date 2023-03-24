<script>
export default {
    data() {
        return {
            dcComicsLinks: [
                "Character",
                "Comics",
                "Movies",
                "TV",
                "Games",
                "Videos",
                "News",
            ],
            dcLinks: [
                "Terms Of Use",
                "Privacy policy (New)",
                "Ad Choises",
                "Advertising",
                "Jobs",
                "Subscriptions",
                "Talent Workshops",
                "CPSC Certificates",
                "Ratings",
                "Shop Help",
                "Contact us",
            ],
            sitesLinks: [
                "DC",
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa",
            ],
            shopLinks: [
                "Shop DC",
                "Shop DC Collectibles"
            ],
        }
    },
}
</script>


<template>
    <footer>
        <div class="container">

            <div class="flex">
                <div>
                    <div class="margin">
                        <strong>DC COMICS</strong>
                    </div>
                    <div>
                        <ul>
                            <li v-for="link in dcComicsLinks"> {{ link }} </li>
                        </ul>
                    </div>
                    <div>
                        <div class="margin">
                        <strong>SHOP</strong>
                    </div>
                    <div>
                        <ul>
                            <li v-for="link in shopLinks"> {{ link }} </li>
                        </ul>
                    </div>
                </div>
                </div>
                <div>
                    <div class="margin">
                        <strong>DC</strong>
                    </div>
                    <div>
                        <ul>
                            <li v-for="link in dcLinks"> {{ link }} </li>
                        </ul>
                    </div>
                </div>
                <div>
                    <div class="margin">
                        <strong>SITES</strong>
                    </div>
                    <div>
                        <ul>
                            <li v-for="link in sitesLinks"> {{ link }} </li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="absolute">
                <img src="/img/dc-logo-bg.png" alt="">
            </div>

        </div>
    </footer>
</template>


<style lang="scss" scoped>

footer {
    background-image: url("/img/footer-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;


    .container {
        position: relative;
        margin: 0 auto;
        max-width: 1200px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        overflow: hidden;

        .flex {
            display: flex;
            flex-wrap: wrap;
            gap: 60px;
            padding: 40px 0 50px;

            .margin {
                margin: 20px 0;

                strong {
                    font-size: 20px;
                    color: white;
                }
            }

            ul {
                list-style-type: none;
                color: #74787b;

                li {
                    font-size: 14px;
                }
            }
        }
        .absolute {
            position: absolute;
            right: 10px;
        
            img {
                transform: rotate(350deg);
                height: auto;
                width: 600px;
                object-fit: cover;
            }
        }
    }
}



</style>