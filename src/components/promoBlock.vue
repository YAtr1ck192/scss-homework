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
            <div class="right-part">
                <img src="/images/promo-img.png" alt="promo-img" >
            </div>
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
            }
        }
        .right-part {
            position: relative;

            img {
                position: absolute;
                right: 0;
                margin-top: -400px;
                margin-right: -50px;
            }
        }
    }
</style>