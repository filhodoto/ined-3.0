<template>
    <div>
        <carousel></carousel>
        <nuxt/>
        <Footer></Footer>
    </div>
</template>
<script>
    import Footer from '@/components/Footer.vue'
    import Carousel from '~/components/Carousel.vue'

    export default {
        components: {
            Footer,
            Carousel
        }
    }
</script>
<style lang="scss">
    #__layout > div:first-of-type {
        display: flex;
        flex-direction: column;
    }
</style>