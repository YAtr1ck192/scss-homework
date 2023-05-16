<template>
    <div class="slide">
        <img :src="slide.img" alt="slide-img" class="slide-img">
        <div class="slide-content">
            <div class="slide-desc">
                {{ slide.desc }}
            </div>
            <div class="hr"></div>
            <div class="user-name">
                {{ slide.userName }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "slideCard",
    props: ['slide']
}
</script>

<style scoped lang="scss">
    @import "src/styles/global";

    .slide {
        max-width: 546px;
        max-height: 247px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;

        .slide-img {
            width: 93px;
            height: 106px;
            z-index: 1;
            margin-bottom: 17px;
        }
        .slide-content {
            background: white;
            border-radius: 9px;
            width: 536px;
            height: 187px;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            padding: 60px 45px 20px;
            
            .slide-desc {
                text-align: center;
            }
            .hr {
                width: 130px;
                height: 2px;
                background: linear-gradient(95.2deg, #B90160 2.23%, #2E3192 100%);
                border-radius: 1px;
            }
        }
    }
</style>