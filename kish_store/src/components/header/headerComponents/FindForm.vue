<template lang="">
    <div class="header__find">
        <form class="header__find-form" action="#">
            <input class="header__find-form--text" type="text" placeholder="Поиск товаров" name="find">
            <button class="header__find-form--btn" value="value-btn">Поиск</button>
        </form>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
    .header__find-form--text {
        background: rgba(217, 217, 217, 0.6);
        border-radius: 10px;
        padding: 10px 12px;
        border: none;
        outline: none;
        color: #000;
        font-weight: 500;
        font-size: 14px;
        line-height: 150%;
        margin-right: 10px;
    }

    .header__find-form--btn {
        background: #800000;
        border: 3px solid #800000;
        border-radius: 10px;
        padding: 9px 12px;
        color: #FFFFFF;
        font-weight: 500;
        font-size: 14px;
        line-height: 150%;
    }
</style>