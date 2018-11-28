<template>
    <section class="container">
        <div>
            <logo/>
            <h1 class="title">
                title
            </h1>
            <div class="links">
                <a
                    class="icon is-large fa-2x"
                    href="https://nuxtjs.org/"
                    target="_blank"><font-awesome-icon :icon="['fab','facebook']" /></a>
                <a
                    class="icon is-large fa-2x"
                    href="https://nuxtjs.org/"
                    target="_blank"><font-awesome-icon :icon="['fab','instagram']" /></a>

            </div>
        </div>
    </section>
</template>

<script>
    import Logo from '~/components/Logo.vue'

    export default {
        components: {
            Logo
        }
    }
</script>

<style lang='scss' scoped>
    @import '~/assets/styles/main.scss';

    .container {
        min-height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .title {
        font-family: $body-font-secondary;
        display: block;
        font-weight: 300;
        font-size: 100px;
        color: #35495e;
        letter-spacing: 1px;
    }

    .subtitle {
        font-weight: 300;
        font-size: 42px;
        color: #526488;
        word-spacing: 5px;
        padding-bottom: 15px;
    }

    .links {
        padding-top: 15px;
    }

    .icon {
        color: black;
    }
</style>
