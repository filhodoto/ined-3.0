<template>
    <div>
        <nuxt/>
        <Footer></Footer>
    </div>
</template>
<script>
    import Footer from '@/components/Footer.vue'

    export default {
        components: {
            Footer
        }
    }
</script>
<style lang="scss">
    #__layout > div:first-of-type {
        display: flex;
        flex-direction: column;
    }
</style>