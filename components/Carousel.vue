<template>
    <transition appear name="fade">
        <aside class="carousel-wrapper">
            <div v-for="image in images" class="bg-image" :style="{ 'background-image': `url(${image.url})`}"></div>
        </aside>
    </transition>
</template>
<script>
    import axios from 'axios';

    export default {
        name: 'carousel',
        data() {
            return {
                images: [],
                currentImg: 0,
                transitionDelay: 6000
            }
        },

        mounted() {
            this.fetchImages();
        },

        beforeDestroy() {
            this.stopCarousel();
        },

        methods: {
            async fetchImages() {
                // Populate state images with API response
                await axios.get(`https://jsonplaceholder.typicode.com/photos`)
                            .then(res => this.images = res.data.slice(0,10))

                // start carousel after we have images
                this.startCarousel();
            },

            startCarousel() {
                let current = 0;
                let slides = document.querySelectorAll('.bg-image');

                this.carouselInterval = setInterval(function() {
                    for (let i = 0; i < slides.length; i++) {
                        slides[i].style.opacity = 0;
                    }
                    current = (current !== slides.length - 1) ? current + 1 : 0;
                    slides[current].style.opacity = 1;
                }, this.transitionDelay);
            },
            stopCarousel() {
                console.log('stopCarousel');
                clearInterval(this.carouselInterval);
            }
        },
        computed: {
            // images () {
            //     return
            // }
        }
    }
</script>
<style lang='scss' scoped>
    .carousel-wrapper {
        position: fixed;
        height: 100%;
        width: 100%;
        opacity: 0.2;
        z-index: -1;
    }

    .bg-image {
        width: 100%;
        height: 100%;
        position: absolute;
        background-repeat: no-repeat;
        background-position: center center;
        background-size: cover;
        background-attachment: fixed;

        transition: opacity 1s ease-in;
    }
</style>
