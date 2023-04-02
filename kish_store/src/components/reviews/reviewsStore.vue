<template>
    <section class="reviews">
        <div class="reviews__inner">
            <h2 class="reviews__title">Отзывы</h2>
            <ul class="reviews__list">
                <li v-for="item in items" :key="item.id">
                    <Review
                    :name="item.name"
                    :product="item.product"
                    :date="item.date"
                    :reviewText="item.reviewText"   
                    />
                </li>
            </ul>
            <div class="review__all-block">
                <a href="#" class="review__all">Читать все отзывы</a>
            </div>
        </div>
    </section>
</template>

<script>
    import Review from './rewiewsComponents/review.vue';

    export default {
        components: {
            Review
        },
        data() {
            return {
                items: [
                    {
                        id: 0,
                        name: 'Антон Курпатов',
                        product: 'Футболка Misfits',
                        date: '24.01.2023',
                        reviewText: 'Товар пришел точно в срок! Отличное соотношение цены и качества'
                    },
                    {
                        id: 1,
                        name: 'Андрей Кузнецов',
                        product: 'Браслет',
                        date: '21.01.2023',
                        reviewText: 'Отличное соотношение цены и качества. Товар пришел точно в срок!'
                    },
                    {
                        id: 2,
                        name: 'Никита Федоров',
                        product: 'Футболка Misfits',
                        date: '01.02.2023',
                        reviewText: 'Товар пришел точно в срок! Отличное соотношение цены и качества'
                    }
                ]
            }
        }
    }
</script>

<style>
    .reviews {
        width: 1440px;
        margin: 0 auto 94px;
        padding: 0 150px;
    }

    .reviews__title {
        font-weight: 700;
        font-size: 26px;
        line-height: 150%;
        color: #000;
        padding: 14px 36px;
        background-color: #F8B101;
        width: 185px;
        margin-bottom: 40px;
    }

    .reviews__list {
        display: flex;
        gap: 46px;
        list-style: none;
    }

    .review__all-block {
        text-align: center;
        margin-top: 30px;
    }

    .review__all {
        font-weight: 400;
        font-size: 26px;
        line-height: 150%;
        text-decoration: underline;
        color: #fff;
    }
</style>