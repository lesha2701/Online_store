<template>
    <div class="hit__block">
        <img class="hit__block-img" :src="img" alt="">
        <div class="hit__block-info">
            <div class="hit__block-info--descr">
                <p class="descr__title">{{ name }}</p>
                <p class="descr__price">{{ price }}</p>
            </div>
            <catalogBtn />
        </div>
    </div>
</template>

<script>
    import catalogBtn from './catalogBtn.vue';
    export default {
        components: {
            catalogBtn
        },
        props: [
            'img',
            'name',
            'price'
        ]
    }
</script>

<style>
    .hit__block {
        display: flex;
        flex-direction: column;
        max-width: 545px;
    }

    .hit__block-img {
        transition: .3s;
    }

    .hit__block-img:hover {
        scale: 0.98;
    }

    .hit__block-info {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-top: 17px;
    }

    .hit__block-info--descr {
        display: flex;
        flex-direction: column;
    }

    .descr__title {
        font-weight: 400;
        font-size: 26px;
        line-height: 150%;
    }

    .descr__price {
        font-weight: 400;
        font-size: 26px;
        line-height: 150%;
        color: #F8B101;
    }
</style>