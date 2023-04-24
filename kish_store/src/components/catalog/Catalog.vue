<template>
    <section class="catalog">
        <div class="catalog__title-block">
            <p class="catalog__title">Каталог</p>
            <img @click="showModalWindow" src="/shopping_cart_icon_245998.svg" alt="">
        </div>
        <div class="modalBlock">
            <modalStore 
            v-if="showModal"
            :carts="cartsItems"
            />
        </div>
        <div class="catalog__inner">
            <div class="catalog__left">
                <p class="catalog__left-title">Хит продаж</p>
                <div v-for="item in itemsHit" :key="item.id">
                    <HistStore
                    :id="item.id" 
                    :img="item.img"
                    :name="item.name"
                    :price="item.price"
                    @send-data-to-parent-hits="receiveDataFromChildHits"
                    />
                </div>
            </div>
            <div class="catalog__right">
                <p class="catalog__right-title">Новые поступления</p>
                <ul class="catalog__right-product">
                    <li v-for="item in itemsNew" :key="item.id">
                        <newStore 
                        :id="item.id"
                        :img="item.img"
                        :name="item.name"
                        :price="item.price"
                        @send-data-to-parent-new="receiveDataFromChildNew"
                        />
                    </li>
                </ul>
            </div>
        </div>
        <div class="catalog__all-block">
            <a href="#" class="catalog__all">Смотреть весь каталог</a>
        </div>
    </section>
</template>

<script>
    import HistStore from './catalogConponents/histStore.vue';
    import newStore from './catalogConponents/newStore.vue';
    import modalStore from '../modalStore.vue';
    import {ref} from 'vue';
    import { useStorage } from '@vueuse/core';

    export default {
        components: {
            HistStore,
            newStore,
            modalStore
        },
        data() {
            return {
                itemsNew: [
                    {
                        id: 0,
                        img: 'catalog/catalog-new.png',
                        name: 'Легендарная кофта Князя1',
                        price: '3 499 руб.',
                    },
                    {
                        id: 1,
                        img: 'catalog/catalog-new.png',
                        name: 'Легендарная кофта Князя2',
                        price: '3 699 руб.',            
                    },
                    {
                        id: 2,
                        img: 'catalog/catalog-new.png',
                        name: 'Легендарная кофта Князя3',
                        price: '2 699 руб.',
                    }
                ],
                itemsHit: [
                    {
                        id: 0,
                        img: 'catalog/catalog-main.jpg',
                        name: 'Футболка Misfits',
                        price: '2 199 руб.',
                    }
                ],
                cartsItems: [],
                idCartsHits: 0,
                idCartsNew: 0,
                showModal: false
            }
        },
        methods: {
            receiveDataFromChildHits(id) {
                this.itemsHit.forEach(element => {
                    if (element.id == id) {
                        const cartItem = {id: this.idCartsHits, img:element.img, name:element.name, price:element.price}
                        this.cartsItems.push(cartItem);
                        this.idCartsHits += 1;
                    }
                })
            },
            receiveDataFromChildNew(id) {
                this.itemsNew.forEach(element => {
                    if (element.id == id) {
                        const cartItem = {id: this.idCartsNew, img:element.img, name:element.name, price:element.price}
                        this.cartsItems.push(cartItem);
                        this.idCartsNew += 1;
                        
                    }
                })
            },
            showModalWindow(e) {
                e.preventDefault()
                if (this.showModal) {
                    this.showModal = false
                } else {
                    this.showModal = true
                }
            }
        },
        setup() {
            const items = ref([])
            const storage = useStorage(localStorage)

            const addItemInCarts = (id, img, name, price) => {
                const newItem = {id: id, img: img, name: name, price: price}
                items.value.push(newItem)
                storage.set('items', items.value)
            }

            if (storage.get('items')) {
                items.value = storage.get('items')
            }

            return {
                items,
                addItemInCarts
            }
        }
    }
</script>
<style>

    .catalog {
        margin-bottom: 160px;
    }

    .catalog__title-block {
        background-color: #F8B101;
        display: flex;
        justify-content: center;
        gap: 30px;
    }

    .catalog__title {
        font-weight: 700;
        font-size: 26px;
        line-height: 150%;
        color: #000;
        padding: 15px 0;
        letter-spacing: 0.205em;
    }

    .modalBlock {
        display: flex;
        justify-content: center;
    }

    .catalog__inner {
        width: 1440px;
        margin: 0 auto;
        padding: 0 150px;
        display: flex;
        justify-content: space-between;
    }

    .catalog__left {
        width: 545px;
    }

    .catalog__left-title {
        text-align: center;
        padding: 6px 46px;
        margin: 47px auto 24px;
        background-color: #F8B101;
        width: 270px;
        font-weight: 700;
        font-size: 26px;
        line-height: 150%;
        color: #000;
    }

    .catalog__right-title {
        text-align: center;
        padding: 6px 46px;
        margin: 47px auto 24px;
        background-color: #F8B101;
        width: 378px;
        font-weight: 700;
        font-size: 26px;
        line-height: 150%;
        color: #000;     
    }

    .catalog__right {
        width: 538px;
    }

    .catalog__right-product {
        display: flex;
        flex-direction: column;
        gap: 30px;
        list-style: none;
    }

    .catalog__all-block {
        text-align: center;
        margin-top: 30px;
    }

    .catalog__all {
        font-weight: 400;
        font-size: 26px;
        line-height: 150%;
        color: #fff;
        text-decoration: underline;
    }
</style>