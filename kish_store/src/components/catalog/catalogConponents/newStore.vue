<template>
    <div class="new__block">
        <img class="new__block-img" :src="img" alt="">
        <div class="new__title-descr">
            <p class="new__title-descr--title">{{ name }}</p>
            <p class="new__title-descr--price">{{ price }}</p>
            <orderBtn 
            :info="info"
            @click="getInfo"
            />
        </div>
    </div>
</template>

<script>
    import orderBtn from '../../orderBtn.vue'

    export default {
        components: {
            orderBtn
        },
        props: [
            'img',
            'name',
            'price'
        ],
        data() {
            return {
                info: {}
            }
        },
        methods: {
            getInfo() {
                this.info = {
                    img: 'catalog/catalog-main.jpg',
                    name: this.name,
                    price: this.price
                }
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