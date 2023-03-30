<template>
    <div class="preloader">
        <img class="preloader__shut" src="shut.png" alt="">
        <div class="hands">
            <img class="preloader__l-hand" src="l_hand.png" alt="">
            <img class="preloader__r-hand" src="r_hand.png" alt="">
        </div>
        <img class="preloader__ksh" src="ksh.png" alt="">
    </div>
</template>

<script>

</script>

<style>
    .preloader {
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        position: relative;
    }

    .hands {
        display: flex;
        gap: 282px;
        position: relative;
        top: 122px;
    }

    .preloader__shut {
        position: absolute;
        top: 200px;
    }

    .preloader__l-hand {
        position: relative;
        top: -25px;
    }

    .preloader__ksh {
        max-width: 735px;
        position: relative;
        top: 128px;
    }
</style>