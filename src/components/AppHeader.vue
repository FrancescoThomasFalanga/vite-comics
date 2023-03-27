<script>
import AppCard from "./AppCard.vue"

export default {
    data() {
        return {
            dcCards: [
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://picsum.photos/100",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                }
            ],
        }
    },

    components: {
        AppCard,
    },
}
</script>


<template>
    <header>

        <div class="bg-img"></div>

        <div class="container">
            <AppCard v-for="card in dcCards" class="ciao" :thumb="card.thumb" :title="card.series"></AppCard>

            <div class="absolute">CURRENT SERIES</div>
        </div>

        <div class="more">
            <a href="">LOAD MORE</a>
        </div>
    </header>
</template>


<style lang="scss" scoped>

header {
    background-color: #1c1c1c;

    .bg-img {
        background-image: url("/img/jumbotron.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        height: 400px;
    }

    .container {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        max-width: 1200px;
        margin: 0 auto;
        padding: 30px 0;
        color: white;

        .absolute {
            position: absolute;
            top: -23px;
            left: 0;
            padding: 8px 30px;
            font-weight: bold;
            font-size: 20px;
            background-color: #0282f9;
        }
    }

    .more {
        text-align: center;
        padding-bottom: 20px;

        a {
            padding: 6px 60px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            background-color: #0282f9;
        }
    }

}

</style>