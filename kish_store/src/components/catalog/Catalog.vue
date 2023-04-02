<template>
    <section class="catalog">
        <p class="catalog__title">Каталог</p>
        <div class="catalog__inner">
            <div class="catalog__left">
                <p class="catalog__left-title">Хит продаж</p>
                <HistStore 
                :img="imgHit"
                :name="nameHit"
                :price="priceHit"
                />
            </div>
            <div class="catalog__right">
                <p class="catalog__right-title">Новые поступления</p>
                <ul class="catalog__right-product">
                    <li v-for="item in items" :key="item.id">
                        <newStore 
                        :img="item.img"
                        :name="item.name"
                        :price="item.price"
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

    export default {
        components: {
            HistStore,
            newStore
        },
        data() {
            return {
                items: [
                    {
                        id: 0,
                        img: 'catalog/catalog-new.png',
                        name: 'Легендарная кофта Князя1',
                        price: '3 499 руб.'
                    },
                    {
                        id: 1,
                        img: 'catalog/catalog-new.png',
                        name: 'Легендарная кофта Князя2',
                        price: '3 699 руб.'                 
                    },
                    {
                        id: 2,
                        img: 'catalog/catalog-new.png',
                        name: 'Легендарная кофта Князя3',
                        price: '2 699 руб.'       
                    }
                ],

                imgHit: 'catalog/catalog-main.jpg',
                nameHit: 'Футболка Misfits',
                priceHit: '2 199 руб.'
            }
        }
    }
</script>
<style>

    .catalog {
        margin-bottom: 160px;
    }

    .catalog__title {
        background-color: #F8B101;
        text-align: center;
        font-weight: 700;
        font-size: 26px;
        line-height: 150%;
        color: #000;
        padding: 15px 0;
        letter-spacing: 0.205em;
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