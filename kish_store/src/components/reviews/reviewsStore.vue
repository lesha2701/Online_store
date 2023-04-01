<template>
    <section class="reviews">
        <div class="reviews__inner">
            <h2 class="reviews__title">Отзывы</h2>
            <div class="reviews__list">
                <Review />
                <Review />
                <Review />
            </div>
            <div class="review__all-block">
                <a href="#" class="review__all">Читать все отзывы</a>
            </div>
        </div>
    </section>
</template>

<script setup>
import Review from './rewiewsComponents/review.vue';
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