<template>
    <header>
        <headerSocial />
        <div class="container">
            <div class="header-content">
                <a href="#">
                    <img src="/images/header-logo.png" alt="header-logo" class="header-logo">
                </a>
                <nav>
                    <a href="#" class="nav-item">отзывы</a>
                    <a href="#" class="nav-item">что это?</a>
                    <a href="#" class="nav-item">контакты</a>
                </nav>
            </div>
        </div>
    </header>
</template>

<script>
import headerSocial from '@/components/headerSocial.vue'
export default {
    name: "headerBlock",
    components: {
        headerSocial
    }
}
</script>

<style scoped lang="scss">
    @import "src/styles/global";
    .header-content {
        margin-top: 50px;
        display: flex;
        align-items: flex-start;
        justify-content: space-between;

        a .header-logo {
            width: 270px;
            height: 60px;
        }
        nav {
            .nav-item {
                @include defaultGreyText;
                margin-left: 25px;
                font-size: 18px;

                &:first-child {
                    margin-left: 0;
                }
            }
        }
    }
</style>