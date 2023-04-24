<template>
    <div class="hit__block">
        <img class="hit__block-img" :src="img" alt="">
        <div class="hit__block-info">
            <div class="hit__block-info--descr">
                <p class="descr__title">{{ name }}</p>
                <p class="descr__price">{{ price }}</p>
            </div>
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
        data() {
            return {
                item: {
                    id: this.id,
                    img: this.img,
                    name: this.name,
                    price: this.price
                }
            }
        },
        methods: {
            addProductInCarts() {
                this.$emit('send-data-to-parent-hits', this.item)
            }
        }
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

    .order {
        padding: 7px 20px;
        background-color: #F8B101;
        color: #000000;
        font-weight: 400;
        font-size: 24px;
        line-height: 150%;
        text-decoration: none;
    }
</style>