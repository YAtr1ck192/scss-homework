<template>
    <div class="container">
        <div class="desc-block-content">
            <h2 class="desc-block-title">
                Что такое <span class="gradient-text">EVA</span> коврики?
            </h2>
            <div class="desc-block-cards">
                <descBlockCard
                    v-for="(card, index) in cards"
                    :key="index"
                    :card="card"
                />
            </div>
            <img
                src="/images/desc-block-right-decor.png"
                alt="desc-block-decor"
                class="desc-block-decor right-decor"
            >
            <img
                src="/images/desc-block-decor.png"
                alt="desc-block-decor"
                class="desc-block-decor left-decor"
            >
        </div>
    </div>
</template>

<script>
import descBlockCard from "@/components/descBlockCard.vue";
export default {
    name: "materialDescBlock",
    data () {
        return {
            cards: [
                {
                    img: '/images/desc-block-card-img-1.png',
                    title: 'МАТЕРИАЛ',
                    desc:
                        'Коврики EVA всесезонные и отличаются' +
                        ' уникальной поверхностью материала с' +
                        ' ячейками ромбовидной формы. Из-за чего' +
                        ' вода не проливается при изъятии ковра и' +
                        ' не плещется при езде. Коврики воду не' +
                        ' пропускают.'
                },
                {
                    img: '/images/desc-block-card-img-2.png',
                    title: 'ОТЛИЧИЯ',
                    desc:
                        'Резиновые коврики загибаются и лезут на' +
                        ' педали. EVA коврики такого не допустят!' +
                        ' Специальные липучки держат его в одном' +
                        ' положении. При желании, для водителя' +
                        ' устанавливается подпятник из рельефного ' +
                        'алюминия.'
                },
                {
                    img: '/images/desc-block-card-img-3.png',
                    title: 'РАСЦВЕТКА',
                    desc:
                        'Автомобильные коврики EVA можно' +
                        ' заказать и в индивидуальных размерах и в' +
                        ' разных цветах, которые комбинируется на' +
                        ' выбор покупателя с такими же цветами' +
                        ' окантовочной полипропиленовой ременной' +
                        ' ленты.'
                }
            ]
        }
    },
    components: {
        descBlockCard
    }
}
</script>

<style scoped lang="scss">
    @import "src/styles/global";

    .desc-block-content {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        padding: 25px 0 225px;

        .desc-block-title {
            font-family: 'Roboto', sans-serif;
            font-size: 50px;
            font-weight: 400;
            line-height: 59px;
            text-align: center;
            margin-bottom: 120px;

            .gradient-text {
                background-image: $linearGradient;
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;
            }
        }
        .desc-block-cards {
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: $maxWidth - 30;
            z-index: 4;
        }
        .desc-block-decor {
            position: absolute;
            z-index: -1;
            width: 757px;
            height: 581px;
        }
        .left-decor {
            margin-top: 330px;
            margin-left: -150px;
            left: 0;
        }
        .right-decor {
            display: none;
        }
    }
    @media screen and (max-width: $tabletWidth){
        .desc-block-content {
            padding: 100px 0 65px;

            .desc-block-title {
                font-size: 40px;
                line-height: 47px;
                margin-bottom: 50px;

            }
            .desc-block-cards {
                width: $maxWidthTablet - 30;
                flex-wrap: wrap;
                z-index: 4;
            }
            .desc-block-decor {
                width: 232px;
                height: 200px;
            }
            .left-decor {
                left: 35px;
                margin-top: -420px;
            }
            .right-decor {
                display: block;
                right: 0;
                margin-right: -80px;
                bottom: -30px;

            }
        }
    }
    @media screen and (max-width: $phoneWidth){
          .desc-block-content {
              padding: 0 0 65px;

              .desc-block-title {
                  font-size: 20px;
                  line-height: 24px;
              }
              .desc-block-cards {
                  width: 265px;
              }
              .desc-block-decor {
                  display: none;
              }
          }
    }
</style>
