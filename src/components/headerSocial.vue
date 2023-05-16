<template>
    <div class="header-social">
        <div class="container">
            <div class="header-social-content">
                <div class="social-block">
                    <img 
                        src="../../public/images/header-phone-icon.png"
                        alt="header-phone-icon"
                        class="phone-icon"
                    >
                    <a href="#" class="social-link">+375 29 292-29-29 (VEL)</a>
                    <a href="#" class="social-link">+375 33 333-33-33 (МТС)</a>
                </div>
                <div class="social-block">
                    <img
                        src="/images/header-location-icon.png"
                        alt="header-location-icon"
                        class="location-icon"
                    >
                    <a href="#" class="social-link">ваш город</a>
                </div>
                <div class="social-block">
                    <img
                            src="/images/header-social-icon.png"
                            alt="header-social-icon"
                            class="social-icon"
                    >
                    <a href="#" class="social-link">
                        посетите нашу <br>
                        страницу
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "headerSocial"
}
</script>

<style scoped lang="scss">
    @import "src/styles/global";
    .header-social {
        background: linear-gradient(269.91deg, rgba(46, 49, 146, 0.7) 0%, rgba(212, 20, 90, 0.7) 98.16%);
        max-height: 77px;
        min-width: 100%;

            .header-social-content {
                padding: 20px 0;
                display: flex;
                align-items: center;
                justify-content: space-between;
                .social-block {
                    display: flex;
                    align-items: center;

                    &:nth-child(2) {
                        width: 340px;
                    }
                    .phone-icon {
                        width: 20px;
                        height: 20px;
                    }
                    .location-icon {
                        width: 15px;
                        height: 25px;
                    }
                    .social-icon {
                        width: 30px;
                        height: 30px;
                    }
                    .social-link {
                        @include defaultWhiteText;
                        margin-left: 12px;
                    }
                }
            }

    }
</style>