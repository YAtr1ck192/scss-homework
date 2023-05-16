<template>
    <div class="slider-wrapper">
        <swiper class="swiper container" :options="swiperOption" :social="social.content">
            <swiper-slide
                    v-for="(slide, index) in social.content"
                    :key="index"
            >
                <a :href="slide.link"><img :src="slide.icon" alt="slide"/></a>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
    name: "sliderWrapper"
}
</script>

<style scoped>

</style>