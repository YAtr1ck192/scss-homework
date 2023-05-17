<template>
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
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
import slideCard from "@/components/slideCard";
export default {
    name: "sliderWrapper",
    data () {
        return {
            slides: [
                {
                    img: '/images/slide-img-2.png',
                    desc: 'Покупала у ребят коврики для Хундай солярис в' +
                        ' подарок молодому человеку. Все очень' +
                        ' понравилось. Буду советовать только вас.',
                    userName: 'Вера К.'
                },
                {
                    img: '/images/slide-img-3.png',
                    desc: 'Спасибо, все приехало, поставил. Результатом ' +
                        'доволен, в машине супер! Заказывал на Ниссан.',
                    userName: 'Николай П.'
                },
                {
                    img: '/images/slide-img-1.png',
                    desc: 'Коврики супер!!! Качество на высшем уровне!!!' +
                        'Удачи и побольше заказов вам!!! Большое спасибо!',
                    userName: 'Константин В.'
                },
            ]
        }
    },
    computed: {
        swiperOption() {
            return {
                slidesPerView: 3,
                spaceBetween: 70,
                slidesPerGroup: 1,
                loop: true,
                centeredSlides: true,
                /*breakpoints: {
                    320: {
                        slidesPerView: 1,
                        spaceBetween: 70,
                    },
                    760: {
                        slidesPerView: 1,
                        spaceBetween: 70,
                    },
                    1340: {
                        slidesPerView: 3,
                        spaceBetween: 70,
                    },
                }*/
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
 .swiper-slide {
     opacity: .4;


     &.swiper-slide-active {
         transition: ease-in-out .3s;
         opacity: 1;
     }
 }
</style>
