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
            <div class="promo-main-img">
                <img
                    src="/images/promo-img.png"
                    alt="promo-img"
                >
                <img
                    src="/images/promo-main-decor.png"
                    alt="promo-main-decor"
                >
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
                font-family: 'Roboto', sans-serif;
                font-size: 50px;
                font-weight: 900;
                line-height: 59px;
                text-align: left;
            }
            .promo-desc {
                font-family: 'Roboto', sans-serif;
                font-size: 24px;
                font-weight: 300;
                line-height: 28px;
                margin: 10px 0 20px;
                display: flex;
                align-items: flex-start;
            }
            button {
                @include linearGradientButton;
                cursor: pointer;
                padding: 15px 40px;
            }
        }
        .promo-main-img img {
            position: absolute;
            right: 0;

            &:first-child {
                margin-top: -395px;
                margin-right: 45px;
                width: 533px;
                height: 686px;
            }
            &:last-child {
                width: 745px;
                height: 522px;
                margin-top: -315px;

            }
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
            max-height: 407px;
            padding: 60px 0 120px;

            .left-part {
                .promo-title {
                    max-width: 315px;
                    font-size: 40px;
                    line-height: 40px;
                }
                button {
                    padding: 13px 30px;
                    font-size: 15px;
                }
            }
            .promo-main-img img {
                right: -50px;

                &:first-child {
                    width: 368px;
                    height: 473px;
                    top: 325px;

                }
                &:last-child {
                    width: 525px;
                    height: 368px;
                    top: 305px;
                }
            }
            .promo-block-bottom-decor {
                left: 20px;
                bottom: -35px;
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
            height: 148px;
            margin: 40px 0 55px;
            padding: 0;

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
            .promo-main-img img {

                &:first-child {
                    display: none;
                }
                &:last-child {
                    width: 395px;
                    height: 256px;
                    margin-top: -365px;
                    left: -70px;
                }
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
