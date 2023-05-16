<template>
    <div class="container">
        <div class="promo-content">
            <div class="left-part">
                <h1 class="promo-title">
                    Инновационные коврики
                    для автомобиля
                </h1>
                <p class="promo-desc">в вашем городе</p>
                <button>ЗАКАЗАТЬ</button>
            </div>
            <img
                src="/images/promo-block-bottom-decor.png"
                alt="promo-block-bottom-decor"
                class="promo-block-bottom-decor"
            >
            <img
                src="/images/promo-block-top-decor.png"
                alt="promo-block-top-decor"
                class="promo-block-top-decor"
            >
            <img
                src="/images/promo-img.png"
                alt="promo-img"
                class="promo-main-img"
            >
        </div>
    </div>
</template>

<script>
export default {
    name: "promoBlock"
}
</script>

<style scoped lang="scss">
    @import "src/styles/global";
    .promo-content {
        width: 100%;
        height: 685px;
        display: flex;
        align-items: center;
        justify-content: space-between;

        .left-part {
            .promo-title {
                max-width: 675px;
                font-family: 'Roboto';
                font-size: 50px;
                font-weight: 900;
                line-height: 59px;
                text-align: left;
            }
            .promo-desc {
                @include defaultBlackDesc;
                line-height: 28px;
                margin: 10px 0 20px;
                display: flex;
                align-items: flex-start;
            }
            button {
                @include linearGradientButton;
                cursor: pointer;
            }
        }
        .promo-main-img {
                position: absolute;
                right: 0;
                margin-top: -100px;
                margin-right: -40px;
            }
        .promo-block-bottom-decor {
                position: absolute;
                left: 0;
                bottom: 50px;
                width: 115px;
                height: 130px;
        }
        .promo-block-top-decor {
            position: absolute;
            left: 315px;
            top: 180px;
            width: 64px;
            height: 50px;
        }
    }
</style>