<template>
    <div class="slider">
        <div class="slider-track">
            <div class="slider-overflow">
                <sliderWrapper/>
            </div>
        </div>
    </div>
</template>

<script>
import sliderWrapper from "@/components/sliderWrapper";
export default {
    name: "sliderBlock",
    data () {
        return {

        }
    },
    components: {
        sliderWrapper
    }
}
</script>

<style scoped lang="scss">
    @import "src/styles/global";
    .slider {
        width: 100%;
        height: 357px;
        background: linear-gradient(95.2deg, rgba(185, 1, 96, 0.25) 2.23%, rgba(46, 49, 146, 0.25) 100%);
        padding: 55px 0;
        overflow: hidden;

        .slider-overflow {


            .slider-track {
                max-width: 1748px;
                max-height: 247px;
                margin: 0 auto;
                overflow: visible;
            }
        }

    }
</style>
