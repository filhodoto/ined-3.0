<template>
    <section class="wrapper">
        <logo class="logo"/>
        <h2 class="subtitle">Somos um estudio constituido por
            <mark>várias actividades</mark>
             que convergem na 
            <mark>publicidade</mark>
            e o nosso alvo é promover as marcas dos clientes
        </h2>
        <section class="intro">
            <hr>
            <p>A IN.ED é um estúdio, sediado nas Caldas da Rainha, que actua no mercado da publicidade e do design. Qualidade e criatividade são as palavras que melhor nos definem e é graças a estas que vamos marcando pela diferença num mercado de trabalho cada vez mais exigente e competitivo.</p>
            <p class="contacts">Contacte-nos através do nosso email <a href="mailto:geral@ined.com.pt" target="_blank">geral@ined.com.pt</a> ou telefone <a href="tel:00351968274676" target="_blank">968 274 676</a></p>
        </section>
        <ul class="links">
            <li>
                <button-component
                        class="facebook is-large"
                        :icon="['fab','facebook']"
                        text="Facebook"
                        :link="'https://www.facebook.com/ined.com.pt'"
                        :size="'is-medium'">

                </button-component>
            </li>
            <li>
                <button-component
                        class="instagram is-large"
                        :icon="['fab','instagram']"
                        text="Instagram"
                        :link="'https://www.instagram.com/ined.publicidade/'"
                        :size="'is-medium'">

                </button-component>
            </li>
        </ul>
    </section>
</template>

<script>
    import Logo from '~/components/Logo.vue'
    import ButtonComponent from '~/components/ui/Button'

    export default {
        components: {
            Logo,
            ButtonComponent
        }
    }
</script>

<style lang='scss' scoped>
    @import '~/assets/styles/main.scss';

    .wrapper {
        display: flex;
        flex-direction: column;
        flex: 1;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 10px 20px;

        & > * {
            /*border: 1px solid red;*/

            @include respond-to(medium) {
                max-width: 80%;
            }
        }
    }

    .logo {
        margin-bottom: 50px;
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
        font-size: 25px;
        margin: 0;
        word-spacing: 1px;

        @include respond-to(medium) {
            font-size: 35px;
        }
    }

    .intro {
        font-size: 17px;
        display: flex;
        flex-direction: column;
        align-items: center;

        p {
            padding: 5px 0;
        }


        @include respond-to(medium) {
            max-width: 70%;
        }

        hr {
            width: 80%;
            border: none;
        }
    }

    mark {
        background: none;
        font-weight: 700;
    }

    .links {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        margin-top: 40px;
        width: 100%;

        @include respond-to(small) {
            width: auto;
            flex-direction: row;
        }

        li {
            padding: 0 10px;
            margin-top: 20px;
            width: 100%;

            @include respond-to(xsmall) {
                width: auto;
            }

            .button {
                width: 100%;

                @include respond-to(xsmall) {
                    width: auto;
                }
            }
        }
    }

    .icon {
        color: $color-secondary;
        transition: color 0.3s ease-in-out;

        &:hover {
            color: $color-primary;
        }
    }
</style>
