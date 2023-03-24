<script>
export default {
    data() {
        return {
            followLinks: [
                "/img/footer-facebook.png",
                "/img/footer-twitter.png",
                "/img/footer-youtube.png",
                "/img/footer-pinterest.png",
                "/img/footer-periscope.png",
            ],
        }
    },
}
</script>


<template>
    <footer>
        
        <div class="container">

            <div class="something">
                <a href="">SIGN-UP NOW!</a>
            </div>

            <div class="flex">
                <div>
                    <span>FOLLOW US</span>
                </div>
                <div>
                    <ul>
                        <li v-for="link in followLinks"> <a href=""><img :src="link" alt=""></a></li>
                    </ul>
                </div>
            </div>

        </div>

    </footer>
</template>


<style lang="scss" scoped>

footer {
    padding: 30px 0;
    background-color: #303030;

    .container {
        margin: 0 auto;
        max-width: 1200px;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .something {
            a {
                padding: 10px;
                font-size: 14px;
                font-weight: bold;
                text-decoration: none;
                border: 2px solid #057dec;
                color: white;
    
                &:hover {
                    background-color: #057dec;
                    border: 2px solid #1c1c1c88;
                    box-shadow: 1px 4px 5px #057dec;
                }
            }
        }


        .flex {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;

            span {
                font-weight: bold;
                color: #057dec;
            }

            ul {
                display: flex;
                list-style-type: none;

                li {
                    padding: 10px;
                }
            }
        }

    }
}

</style>