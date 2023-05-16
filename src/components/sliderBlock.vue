<template>
    <div class="slider">
        <slideCard
            v-for="(slide, index) in slides"
            :key="index"
            :slide="slide"
        />
    </div>
</template>

<script>
import slideCard from "@/components/slideCard.vue";
export default {
    name: "sliderBlock",
    data () {
        return {
            slides: [
                {
                    img: '/images/slide-img-2.png',
                    desc: 'Покупала у ребят коврики для Хундай солярис в' +
                        ' подарок молодому человеку. Все очень' +
                        ' понравилось. Буду советовать только вас.',
                    userName: 'Вера К.'
                }
            ]
        }
    },
    components: {
        slideCard,
    }
}
</script>

<style scoped lang="scss">
    @import "src/styles/global";
    .slider {
        width: 100%;
        height: 357px;
        background: linear-gradient(95.2deg, rgba(185, 1, 96, 0.25) 2.23%, rgba(46, 49, 146, 0.25) 100%);
    }
</style>