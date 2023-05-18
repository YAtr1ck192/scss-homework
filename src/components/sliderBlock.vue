<template>
    <div class="slider">
        <div
            v-if="screenWidth > 1320"
            class="slider-track"
        >
            <sliderWrapper :slides="slides"/>
        </div>
        <div
            v-if="screenWidth < 1320"
            class="slider-on-media"
        >
            <slideCard
                v-for="(slide, index) in slides"
                :key="index"
                :slide="slide"
                class="slide"
            />
        </div>
    </div>
</template>

<script>
import sliderWrapper from "@/components/sliderWrapper";
import slideCard from "@/components/slideCard";
export default {
    name: "sliderBlock",
    data () {
        return {
            slides: [
                {
                    img: '/images/slide-img-1.png',
                    desc: 'Коврики супер!!! Качество на высшем уровне!!!' +
                        'Удачи и побольше заказов вам!!! Большое спасибо!',
                    userName: 'Константин В.'
                },
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

            ]
        }
    },
    components: {
        sliderWrapper,
        slideCard
    },
        computed: {
        screenWidth: function () {
            return window.screen.width
        }

    }
}
</script>

<style scoped lang="scss">
    @import "src/styles/global";
    .slider {
        width: 100%;
        min-height: 357px;
        background: linear-gradient(95.2deg, rgba(185, 1, 96, 0.25) 2.23%, rgba(46, 49, 146, 0.25) 100%);
        padding: 55px 0;
        overflow: hidden;

        .slider-track {
            max-width: 1748px;
            max-height: 247px;
            margin: 0 auto;
            overflow: visible;
        }
    }
    @media screen and (max-width: $tabletWidth){
        .slider {
            padding: 40px 0 20px;
            .slider-on-media {
                margin: 0 auto;
                max-width: 536px;

                .slide {
                    margin-bottom: 50px;
                }
            }
        }
    }
    @media screen and (max-width: $phoneWidth){
        .slider {

            .slider-on-media {
                max-width: 270px;

                .slide {
                    margin-bottom: 25px;
                }
            }
        }
    }
</style>
