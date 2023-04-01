<template>
    <footer class="footer">
        <div class="footer__inner">
            <img class="footer__img" src="shut.png" alt="">
            <div class="fuuter__text">
                <p class="footer__text-p">Автор: Тюленев Алексей, 2 курс</p>
                <p class="footer__text-p">Интернет-магазин “Король и Шут”</p>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    
}
</script>

<style>
    .footer {
        height: 165px;
        background-color: #F8B101;
    }

    .footer__inner {
        max-width: 1440px;
        margin: 0 auto;
        padding: 0 300px;
        display: flex;
        justify-content: space-between;
        height: 165px;
        overflow: hidden;
    }

    .fuuter__text {
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .footer__img {
        position: relative;
        top: 14px;
        width: 385px;
        height: 247px;
    }

    .footer__text-p {
        font-weight: 400;
        font-size: 20px;
        line-height: 150%;
        color: black;
    }
</style>