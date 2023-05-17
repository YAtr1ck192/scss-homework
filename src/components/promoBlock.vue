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
    @media screen and (max-width: $tabletWidth) {
        .promo-content {
            height: 473px;

            .left-part {
                .promo-title {
                    max-width: 315px;
                }
                button {
                    padding: 13px 30px;
                    font-size: 15px;
                }
            }
            .promo-main-img {
                width: 380px;
                height: 473px;
            }
            .promo-block-bottom-decor {
                left: 20px;
                bottom: -70px;
                width: 100px;
                height: 130px;
                transform: rotate(310deg);
            }
            .promo-block-top-decor {
                top: -35px;
                left: 185px;
            }
        }
    }
    @media screen and (max-width: $phoneWidth) {
        .promo-content {
            height: 256px;

            .left-part {
                margin: 0 auto;
                display: flex;
                align-content: center;
                justify-content: center;
                flex-direction: column;

                .promo-title {
                    max-width: 200px;
                    text-align: center;
                    font-size: 25px;
                    line-height: 25px;
                }
                .promo-desc {
                    font-size: 20px;
                    font-weight: 300;
                    line-height: 23px;
                    text-align: center;
                    margin: 10px auto;
                }
                button {
                    padding: 9px 20px;
                    font-size: 10px;
                    line-height: 12px;
                    width: 93px;
                    margin: 0 auto;
                }
            }
            .promo-main-img {
                display: none;
            }
            .promo-block-bottom-decor {
                display: none;
            }
            .promo-block-top-decor {
                display: none;
            }
        }
    }
</style>
