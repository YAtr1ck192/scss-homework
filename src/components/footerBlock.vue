<template>
    <footer>
       <div class="container">
           <img
               src="/images/footer-left-decor.png"
               alt="footer-decor"
               class="footer-decor left-decor"
           >
           <div class="footer-content">
                <div class="footer-items">
                    <div class="footer-items-title">МЫ В СОЦИАЛЬНЫХ СЕТЯХ</div>
                    <a href="#">
                        <img
                            src="/images/footer-social-icon.png"
                            alt="footer-social-icon"
                            class="footer-social-icon"
                        >
                    </a>
                </div>
                <div class="footer-items">
                   <div class="footer-items-title">КОНТАКТНЫЕ ТЕЛЕФОНЫ</div>
                    <a href="#" class="footer-link">+375 29 292-29-29 (VEL)</a>
                    <a href="#" class="footer-link">+375 33 333-33-33 (МТС)</a>
               </div>
               <div class="footer-items">
                   <div class="footer-items-title">О НАС</div>
                   <a href="#" class="footer-link">Индивидуальное изготовление EVA ковриков для вашего автомобиля</a>
                   <a href="#" class="footer-link town">ваш город</a>
               </div>

           </div>
           <img
               src="/images/footer-right-decor.png"
               alt="footer-decor"
               class="footer-decor right-decor"
           >
       </div>
    </footer>
</template>

<script>
export default {
    name: "footerBlock"
}
</script>

<style scoped lang="scss">
    @import "/src/styles/global";
    footer {
        background: white;
        padding: 20px 0 70px;

        .container {
            .footer-decor {
                position: absolute;
            }
            .left-decor {
                left: 0;
                top: 62px;
                width: 110px;
                height: 125px;
            }
            .right-decor {
                right: 0;
                top: 0;
                width: 233px;
                height: 264px;
            }
            .footer-content {
                padding: 150px 0 20px 0;
                display: flex;

                justify-content: space-evenly;

                .footer-items {
                    display: flex;
                    flex-direction: column;

                    .footer-items-title {
                        @include blackBoldText;
                        font-size: 14px;
                        line-height: 16px;
                        margin-bottom: 10px;
                    }
                    .footer-social-icon {
                        max-width: 33px;
                        max-height: 33px;
                    }
                    .footer-link {
                        font-family: 'Roboto';
                        font-weight: 300;
                        text-decoration: none;
                        color: black;
                        font-size: 14px;
                        line-height: 15px;
                        max-width: 224px;
                        margin-bottom: 5px;
                    }
                    .town {
                        margin-top: 15px;
                    }
                }
            }
        }
    }
    @media screen and (max-width: $tabletWidth) {
        footer {
            .container {
                max-width: 740px;

                .left-decor {
                    left: 85px;
                    top: 120px;
                    width: 85px;
                    height: 97px;
                }
                .right-decor {
                    right: 0;
                    top: 120px;
                    width: 40px;
                    height: 45px;
                }
                .footer-content {
                    padding: 150px 0 20px 0;
                    display: flex;
                    justify-content: space-between;

                }
            }
        }
    }
</style>
