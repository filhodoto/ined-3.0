<template>
    <a v-if="link"
       class="button"
       :href="link"
       target="_blank">
        <font-awesome-icon :icon="icon"/>
        <span>{{text}}</span>
    </a>
    <button v-else
            @click="handleClick"
            class="button">
        <font-awesome-icon :icon="icon"/>
        <span>{{text}}</span>
    </button>
</template>

<script>
    export default {
        name: "button",

        props: ['handleClick', 'link', 'icon', 'text']
    }
</script>

<style lang="scss" scoped>
    @import '~/assets/styles/main.scss';

    .button {
        transition: all 0.3s ease-in-out;

        .icon {
            font-size: 25px;
        }

        &.facebook:hover {
            border-color: $color-facebook;
            color: $color-facebook;
        }

        &.instagram:hover {
            border-color: $color-instagram;
            color: $color-instagram;
        }

        span {
            font-size: 15px;
            margin-left: 10px;
        }
    }
</style>