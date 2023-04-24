<template>
    <div class="hit__block-info--btn">
        <a href="#" class="order" @click.prevent="addProductInCarts">Заказать</a>
        <modalOrder v-if="isModalOpen" @close="closeModal"
        :img="info.img"
        :name="info.name"
        :price="info.price"
        />
    </div>
</template>

<script>
    import modalOrder from './modalOrder.vue'; 
    export default {
        components: {
            modalOrder
        },
        props: ['info'],
        data() {
            return {
                isModalOpen: false
            }
        },
        methods: {
            addProductInCarts(e) {
                e.preventDefault()
                
            },
            closeModal() {
                this.isModalOpen = false
            }
        }
    }
</script>

<style>
    .order {
        padding: 7px 20px;
        background: #F8B101;
        font-weight: 400;
        font-size: 24px;
        line-height: 150%;
        color: #000;
        text-decoration: none;
    }
</style>