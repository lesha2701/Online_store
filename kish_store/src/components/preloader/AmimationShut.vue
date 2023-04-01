<template>
    <div class="preloader">
        <img class="preloader__shut" src="shut.png" alt="">
        <div class="hands">
            <img ref="heading" class="preloader__l-hand" src="l_hand.png" alt="">
            <img class="preloader__r-hand" src="r_hand.png" alt="">
        </div>
        <img class="preloader__ksh" src="ksh.png" alt="">
    </div>
</template>

<script>
    import {gsap} from 'gsap';

export default {

    mounted() {
        const tl = gsap.timeline();

        tl.
        from('.preloader__shut', {
            opacity: 0,
            duration: 2
        })

        tl
        .from('.preloader__l-hand', {
            opacity: 0,
            x: 100,
            y: -50,
            scale: 0.3,
            duration: 1.5,
            ease: "power1.out"
        })
        .from('.preloader__r-hand', {
            opacity: 0,
            x: -100,
            y: -50,
            scale: 0.3,
            duration: 1.5,
            ease: "power1.out"          
        }, '-=1.5')
        .to ('.preloader__shut', {
            scale: 1.1,
            duration: 1.5,
            ease: "power1.out" 
        }, '-=1.5')

        tl
        .from('.preloader__ksh', {
            opacity: 0,
            y: 50,
            duration: 2,
            ease: 'power2.out'
})
    },
}
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
        top: -80px;
    }

    .preloader__l-hand {
        position: relative;
        top: -25px;
    }

    .preloader__ksh {
        max-width: 735px;
        position: relative;
        top: -70px;
    }
</style>