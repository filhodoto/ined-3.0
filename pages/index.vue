<template>
    <section class="wrapper">
        <logo class="logo"/>
        <transition appear name="fade">
            <h2 class="intro">Somos um estudio constituido por
                <mark>várias actividades</mark>
                 que convergem na 
                <mark>publicidade</mark>
                e o nosso alvo é promover as marcas dos clientes
            </h2>
        </transition>
        <transition appear name="fade">
            <section class="description">
                <hr>
                <p>A IN.ED é um estúdio, sediado nas Caldas da Rainha, que actua no mercado da publicidade e do design.
                    Qualidade e criatividade são as palavras que melhor nos definem e é graças a estas que vamos marcando
                    pela diferença num mercado de trabalho cada vez mais exigente e competitivo.</p>
                <ul class="contacts">
                    <li class="contacts-item">
                        <font-awesome-icon :icon="['fas', 'envelope']"/>
                        <a href="mailto:geral@ined.com.pt">geral@ined.com.pt</a>
                    </li>
                    <li class="contacts-item">
                        <font-awesome-icon :icon="['fas', 'phone']"/>
                        <a href="tel:00351968274676">968 274 676</a>
                    </li>
                </ul>
            </section>
        </transition>
        <transition appear name="fade">
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
        </transition>
    </section>
</template>

<script>
    import Logo from '~/components/Logo.vue'
    import ButtonComponent from '~/components/ui/Button'

    export default {
        components: {
            Logo,
            ButtonComponent
        },

        data() {
            return {
                show: false
            }
        },

        mounted() {
          this.show = true;
        }
    }
</script>

<style lang='scss' scoped>
    @import '~/assets/styles/main.scss';
    $transition-duration: 1.5s;

    .wrapper {
        display: flex;
        flex-direction: column;
        flex: 1;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 10px 20px;

        & > * {

            @include respond-to(medium) {
                max-width: 80%;
            }
        }
    }

    .logo {
        margin-bottom: 50px;
    }

    .intro {
        font-weight: 300;
        font-size: 25px;
        margin: 0;
        word-spacing: 1px;
        line-height: 140%;
        transition-duration: $transition-duration;

        @include respond-to(medium) {
            font-size: 35px;
            line-height: 120%;
        }
    }

    .description {
        font-size: 17px;
        display: flex;
        flex-direction: column;
        align-items: center;
        transition-delay: 0.5s;
        transition-duration: $transition-duration;

        @include respond-to(medium) {
            max-width: 70%;
        }

        p {
            padding: 5px 0;
        }

        .contacts {
            display: flex;
            flex-direction: column;
            align-items: center;

            @include respond-to(xsmall) {
                flex-direction: row;
            }


            .contacts-item {
                padding: 15px 15px 0;
                font-size: 18px;
            }

            a {
                color: $color-secondary;
                margin-left: 5px;
            }
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
        transition-delay: 1s;
        transition-duration: $transition-duration;

        @include respond-to(xsmall) {
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
