<template>
    <header class="header">
        <div class="header__inner">
            <div class="header__left">
                <img class="header__shut" src="shut.png" alt=""> 
                <NavItems />     
            </div>
            <div class="header__right">
                <a href="#" class="header__profile">Профиль</a>
            </div>
        </div>
    </header>
</template>

<script>
import FindForm from './headerComponents/FindForm.vue';
import NavItems from './headerComponents/NavItems.vue';

export default {
    components: {
        FindForm,
        NavItems
    }

}
</script>

<style>
    .header {
        height: 120px;
        background-color: #F8B101;
    }

    .header__inner {
        max-width: 1440px;
        margin: 0 auto;
        padding: 20px 180px;
        display: flex;
        justify-content: space-between;
    }

    .header__left {
        display: flex;
        align-items: center;
        gap: 60px;
    }

    .header__shut {
        width: 124px;
    }

    .header__right {
        display: flex;
        align-items: center;
        gap: 60px;
    }

    .header__profile {
        font-weight: 500;
        font-size: 14px;
        line-height: 150%;
        color: #2E363E;
        text-decoration: none;
    }
</style>