<template>
    <div class="container">
        <div class="slider-wrapper">
            <swiper class="swiper" :options="swiperOption">
                <swiper-slide
                    v-for="(slide, index) in slides"
                    :key="index"
                >
                    <slideCard :value="slide" :slide="slide"/>
                </swiper-slide>
            </swiper>
        </div>
    </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
import slideCard from "@/components/slideCard";
export default {
    name: "sliderWrapper",
    props: ['slides'],
    computed: {
        swiperOption() {
            return {
                slidesPerView: 3,
                spaceBetween: 70,
                slidesPerGroup: 1,
                loop: true,
                centeredSlides: true,
            }
        }
    },
    components: {
        Swiper,
        SwiperSlide,
        slideCard
    },

}
</script>

<style scoped lang="scss">
    @import "src/styles/global";
    .slider-wrapper {
        max-width: $maxWidth;


        .swiper {
            width: 1748px;
            margin-left: -263px;

            .swiper-slide {
                opacity: .4;
                max-width: 536px;

                &.swiper-slide-active {
                    transition: ease-in-out .3s;
                    opacity: 1;
                }
            }
        }

    }



</style>
