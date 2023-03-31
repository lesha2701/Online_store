<template>
    <nav class="header__nav">
        <ul class="header__nav-items">
            <li class="header__nav-item"><a href="#">О магазине</a></li>
            <li class="header__nav-item"><a href="#">Каталог</a></li>
            <li class="header__nav-item"><a href="#">Отзывы</a></li>
        </ul>
    </nav>  
</template>
<script>
export default {
    
}
</script>

<style>
    .header__nav-items {
        display: flex;
        list-style: none;
        gap: 40px;
    }

    .header__nav-item a {
        text-decoration: none;
        font-family: "Montserrat";
    }
</style>