<template>
    <section class="about">
        <div class="about__inner">
            <div class="about__left">
                <h2 class="about__title">О магазине</h2>
                <p class="about__descr about__top">Данный интернет-магазин посвящен группе <span>“Король и Шут”</span> - культовый на постсоветском пространстве коллектив, чей стиль обычно определяют как folk punk или horror punk. Группа навсегда вошла в историю отечественной музыки и глубоко отпечаталась в сердцах миллионов меломанов...</p>
                <p class="about__descr about__bottom">Здесь вы сможете найти как одежду с символикой группы, так и одежду, которую носили участиники группы</p>
            </div>
            <div class="about__right">
                <img class="about__bg about__absolute" src="Rectangle 3.svg" alt="">
                <img class="about__img about__absolute" src="slider/slider1.jpg" alt="">
            </div>
        </div>
    </section>
</template>

<script>
</script>

<style>
    .about {
        width: 1440px;
        margin: 125px auto 158px;
    }

    .about__inner {
        position: relative;
        margin: 0 150px;
        display: flex;
        justify-content: space-between;
    }

    .about__left {
        margin: auto 0;
        width: 671px;
    }

    .about__title {
        width: 205px;
        color: black;
        font-weight: 700;
        font-size: 26px;
        line-height: 150%;
        background-color: #F8B101;
        padding: 10px 20px;
        margin-bottom: 48px;
    }

    .about__descr {
        font-weight: 400;
        font-size: 19px;
        line-height: 150%;
    }

    .about__right {
        position: relative;
    }

    .about__img {
        position: absolute;
        left: -15px;
        top: 15px;
        width: 371px;
    }

    .about__top {
        margin-bottom: 30px;
        width: 637px;
    }

    .about__top span {
        color: #F8B101;
    }

    .about__bottom {
        width: 627px;
    }
</style>