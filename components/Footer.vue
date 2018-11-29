<template>
    <transition appear name="appear-bottom">
        <footer class="footer">
            <div class="content has-text-centered">
                <!--<ul class="level is-mobile">-->
                    <!--<li class="item"><font-awesome-icon :icon="['fas','envelope']" /> geral@ined.com.pt</li>-->
                    <!--<li class="item">© {{year}} IN.ED - facebook - instagram</li>-->
                    <!--<li class="item"><font-awesome-icon :icon="['fas','phone']" />968 274 676</li>-->
                <!--</ul>-->
                <p>© {{year}} IN.ED - <a href="https://www.facebook.com/ined.com.pt" target="_blank">facebook</a> - <a href="https://www.instagram.com/ined.publicidade/" target="_blank">instagram</a></p>
            </div>
        </footer>
    </transition>
</template>
<script>
    export default {
        data() {
            return {
                year: (new Date()).getFullYear()
            }
        }
    }
</script>
<style lang='scss'>
    @import '~/assets/styles/main.scss';

    $footer-padding: 15px 10px;

    .footer {
        padding: $footer-padding;
        font-size: 13px;
        transition-duration: 1s;

        a {
            text-decoration: underline;
            color: $color-primary;
        }
    }

</style>
