<template>
    <header class="header">
        <div class="header__inner">
            <div class="header__left">
                <img class="header__shut" src="shut.png" alt=""> 
                <NavItems />     
            </div>
            <div class="header__right">
                <a href="#" class="header__profile">Профиль</a>
                <FindForm />
            </div>
        </div>
    </header>
</template>

<script setup>
import FindForm from './headerComponents/FindForm.vue';
import NavItems from './headerComponents/NavItems.vue'
</script>

<style>
    .header {
        height: 120px;
        background-color: #F8B101;
    }

    .header__inner {
        max-width: 1440px;
        margin: 0 auto;
    }

    .header__shut {
        width: 124px;
    }
</style>