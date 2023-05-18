<template>
    <div class="desc-block-card">
        <img :src="card.img" alt="card-img" class="card-img">
        <div class="card-content">
            <h3 class="card-title">{{ card.title }}</h3>
            <div class="card-desc">{{ card.desc }}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: "descBlockCard",
    props: ['card']
}
</script>

<style scoped lang="scss">
    @import "src/styles/global";

    .desc-block-card {
        width: 344px;
        min-height: 414px;
        border-radius: 9px;
        box-shadow: 0 1px 15px #fab8db;
        overflow: hidden;
        display: flex;
        align-items: flex-start;
        justify-content: flex-start;
        flex-direction: column;
        background: white;

        .card-img {
            width: 363px;
            height: 242px;
        }
        .card-content {
            padding: 10px 33px 22px 22px;

            .card-title {
                @include blackBoldText;
                font-size: 36px;
                line-height: 42px;
                margin-bottom: 5px;
            }
            .card-desc {
                @include defaultGreyText;
                font-size: 14px;
            }
        }
    }
    @media screen and (max-width: $tabletWidth) {
        .desc-block-card {
            width: $maxWidthTablet;
            min-height: 325px;
            margin-bottom: 60px;

            .card-img {
                width: $maxWidthTablet;
                height: 160px;
                background-size: cover;
            }
            .card-content {

                .card-desc {
                    max-width: 500px;
                }
            }
        }
    }
    @media screen and (max-width: $phoneWidth) {
        .desc-block-card {
            width: $maxWidthPhone;
            min-height: 360px;
            margin-bottom: 35px;

            .card-img {
                width: $maxWidthPhone;
                height: 180px;
            }
            .card-content {
                padding: 20px;

                .card-title {
                    font-size: 30px;
                    line-height: 35px;
                }
            }
          }
    }
</style>
