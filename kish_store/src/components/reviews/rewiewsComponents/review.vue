<template>
    <div class="review">
        <div class="review__top">
            <div class="review__name">Алексей Петров</div>
            <div class="review__product">Товар: Футболка Misfits</div>
            <div class="review__date">24.01.2023</div>
        </div>
        <div class="review__bottom">
            <p class="review__text">Товар пришел точно в срок! Отличное соотношение цены и качества</p>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
    .review {
        width: 348px;
        display: flex;
        flex-direction: column;
    }

    .review__top {
        padding-left: 17px;
        background-color: #F8B101;
    }

    .review__name {
        margin-top: 3px;
        font-weight: 700;
        font-size: 22px;
        line-height: 150%;
        color: #000;
    }

    .review__product {
        font-weight: 400;
        font-size: 22px;
        line-height: 150%;
        color: #000;
        margin-bottom: 3px;
    }

    .review__date {
        font-weight: 400;
        font-size: 14px;
        line-height: 150%;
        color: #000;
    }

    .review__bottom {
        border: 1px solid #F8B101;
    }
    
    .review__text {
        font-weight: 400;
        font-size: 20px;
        line-height: 150%;
        width: 315px;
        padding-top: 8px;
        padding-left: 14px;
        padding-bottom: 11px;
    }
</style>