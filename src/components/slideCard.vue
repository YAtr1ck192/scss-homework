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
        width: 536px;
        max-height: 247px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-direction: column;

        .slide-img {
            width: 93px;
            height: 106px;
            z-index: 1;
            margin-bottom: -43px;
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
            padding: 55px 46px 20px;

            .slide-desc {
                text-align: center;
                margin-bottom: 20px;
                @include r300;
                font-size: 18px;
                line-height: 21px;
            }
            .hr {
                width: 130px;
                height: 2px;
                background: linear-gradient(95.2deg, #B90160 2.23%, #2E3192 100%);
                border-radius: 1px;
                margin-bottom: 10px;
            }
            .user-name {
                font-family: 'Roboto', sans-serif;
                font-size: 13px;
                font-weight: 300;
                line-height: 15px;
                text-align: center;
                color: #8E8E8E;
            }
        }
    }
    @media screen and (max-width: $phoneWidth) {
        .slide {
            width: 267px;
            max-height: 270px;

            .slide-content {
                width: 267px;
                height: 210px;
                padding: 70px 40px 30px;

                .slide-desc {
                    margin-bottom: 10px;
                    font-size: 12px;
                    line-height: 14px;
                    text-align: center;
                }
            }
        }
    }
</style>
