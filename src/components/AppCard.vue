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
        justify-content: center;
        align-items: center;
        flex-direction: column;
        gap: 10px;
        width: calc(100% / 6);
        padding: 20px;

        span {
            text-transform: uppercase;
            font-size: 14px;
        }
    }

</style>