<template>
    <div class="new__block">
        <img class="new__block-img" :src="img" alt="">
        <div class="new__title-descr">
            <p class="new__title-descr--title">{{ name }}</p>
            <p class="new__title-descr--price">{{ price }}</p>
            <div class="hit__block-info--btn">
                <a href="#" class="order" @click.prevent="addProductInCarts">Купить</a>
            </div>
        </div>
    </div>
</template>

<script>

    export default {
        props: [
            'id',
            'img',
            'name',
            'price'
        ],
        methods: {
            addProductInCarts() {
                this.$emit('send-data-to-parent-new', this.id)
            }
        }
    }
</script>

<style>
    .new__block {
        max-width: 524px;
        display: flex;
        gap: 24px;
    }

    .new__block-img {
        width: 279px;
        transition: .3s;
    }

    .new__block-img:hover {
        scale: 0.98;
    }

    .new__title-descr {
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .new__title-descr--title {
        font-weight: 400;
        font-size: 26px;
        line-height: 150%;
        margin-bottom: 2px;
    }
    
    .new__title-descr--price {
        font-weight: 400;
        font-size: 26px;
        line-height: 150%;
        color: #F8B101;
        margin-bottom: 44px;
    }
</style>