<script>
export default {
    data() {
        return {

        }
    },

    props: {
        thumb: String,
        title: String,
    }
}
</script>


<template>

        <div class="card">
            <img :src="thumb" alt="">
            <span> {{ title }} </span>

        </div>

</template>


<style lang="scss" scoped>

    .card {
        display: flex;
        flex-direction: column;
        gap: 10px;
        width: calc(100% / 6);
        padding: 15px;

        span {
            padding-bottom: 10px;
            text-transform: uppercase;
            font-size: 14px;
        }

        img {
            width: 100%;
            height: 200px;
        }
    }

</style>