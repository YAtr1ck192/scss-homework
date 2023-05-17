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
        height: 414px;
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
                font-family: 'Roboto';
                font-size: 36px;
                font-weight: 700;
                line-height: 42px;
                text-align: left;
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
            width: 594px;
            height: 325px;
            border-radius: 9px;
            box-shadow: 0 1px 15px #fab8db;
            overflow: hidden;
            display: flex;
            align-items: flex-start;
            justify-content: flex-start;
            flex-direction: column;
            background: white;
            margin-bottom: 60px;

            .card-img {
                width: 594px;
                height: 160px;
                background-size: cover;
            }
            .card-content {
                padding: 10px 33px 22px 22px;

                .card-title {
                    font-family: 'Roboto';
                    font-size: 36px;
                    font-weight: 700;
                    line-height: 42px;
                    text-align: left;
                    margin-bottom: 5px;
                }
                .card-desc {
                    @include defaultGreyText;
                    font-size: 14px;
                    max-width: 500px;
                }
            }
        }
    }
</style>
