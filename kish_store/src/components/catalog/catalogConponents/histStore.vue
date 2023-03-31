<template>
    <div class="hit__block">
        <img class="hit__block-img" src="catalog/catalog-main.jpg" alt="">
        <div class="hit__block-info">
            <div class="hit__block-info--descr">
                <p class="descr__title">Футболка Misfits</p>
                <p class="descr__price">2 300 руб.</p>
            </div>
            <div class="hit__block-info--btn">
                <a href="#" class="order">Заказать</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
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
        background: #F8B101;
        font-weight: 400;
        font-size: 24px;
        line-height: 150%;
        color: #000;
        text-decoration: none;
    }
</style>