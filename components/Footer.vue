<template>
    <footer class="footer">
        <div class="content has-text-centered">
            <p>
                © {{year}} IN.ED
            </p>
        </div>
    </footer>
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
    $footer-padding: 15px 10px;
    .footer {
        padding: $footer-padding;
    }
</style>
