<template>
    <section class="container">
        <div>
            <logo class="logo"/>
            <section class="info">
                <h2 class="subtitle">Somos um estudio constituido por <mark>várias actividades</mark> que convergem na <mark>publicidade</mark> e o nosso alvo é promover as marcas dos clientes</h2>

            </section>
            <div class="links">
                <p>Descobre mais sobre nós</p>
                <ul>
                    <li>
                        <a class="level-item icon is-large fa-2x"
                        href="https://nuxtjs.org/"
                        target="_blank"><font-awesome-icon :icon="['fab','facebook']" /></a>
                    </li>
                    <li>
                        <a class="level-item icon is-large fa-2x"
                        href="https://nuxtjs.org/"
                        target="_blank"><font-awesome-icon :icon="['fab','instagram']" /></a>
                    </li>

                    <li>
                        <a class="level-item icon is-large fa-2x"
                        href="https://nuxtjs.org/"
                        target="_blank"><font-awesome-icon :icon="['fas','envelope']" /></a>
                    </li>
                </ul>
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
        display: flex;
        flex: 1;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 10px 20px;
        max-width: 1000px;
    }

    .logo {
        margin-bottom: 20px;
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
        font-size: 20px;
        word-spacing: 5px;

        @include respond-to(medium) {
            font-size: 30px;
        }
    }

    mark {
        background: none;
        font-weight: 700;
    }

    .links {
        padding-top: 15px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;

        ul {
            display: flex;
            align-items: center;
            justify-content: center;
        }
    }

    .icon {
        color: black;
        transition: color 0.5s ease-in-out;
        &:hover {
            color: grey;
        }
    }
</style>
