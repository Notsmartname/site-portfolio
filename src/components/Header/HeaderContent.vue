<template>
    <div class="header__content container" id="home">
        <div class="header__content-main">
            <h1 class="header__content-main-title">
                Web <span>Developer</span>
            </h1>
            <div class="header__content-main-btns">
                <WhiteBtn>Hire me</WhiteBtn>
                <BlackBtn />
            </div>
        </div>
        <div class="header__content-img">
            <img src="/images/circle-around.svg" alt="">
        </div>
    </div>
</template>

<script setup>
import BlackBtn from '@/components/UI/BlackBtn.vue';
import WhiteBtn from '@/components/UI/WhiteBtn.vue';

</script>

<style lang="scss">
.header__content {
    padding-left: 90px;
    display: flex;

    @media (max-width:955.99px) {
        padding-left: 0px;
        position: relative;
        z-index: 1;
        align-items: center;
        justify-content: center;

    }

    &-img {
        display: flex;
        align-items: center;
        justify-content: center;
        filter: brightness(.6);


        @media (max-width:955.99px) {
            position: absolute;
            z-index: -99;
            display: flex;
            align-self: center;
            justify-content: center;
            filter: brightness(.6);

        }

        & img {
            filter: brightness(.6);

            @media (max-width:479.99px) {
                max-height: 250px;
                max-width: 250px;
                height: 100%;
                width: 100%;
            }
        }

    }

    &-main {
        display: flex;
        flex-direction: column;
        padding-top: 202px;
        gap: 48px;

        @media (max-width:955.99px) {
            gap: 24px;
            padding-left: 40px;
        }

        @media (max-width:955.99px) {
            padding-left: 0px;
            padding-top: 152px;

        }



        &-title {
            color: var(--mainColorText);
            font-family: "Poppins";
            font-size: 96px;
            font-weight: 700;
            line-height: 96px;

            @media (max-width:955.99px) {
                font-size: 76px;
                line-height: 76px;

            }

            @media (max-width:575.99px) {
                font-size: 56px;
            }

            @media (max-width:479.99px) {
                font-size: 36px;
            }

            & span {
                color: var(--subMainColorText);
                font-size: 96px;
                font-weight: 700;
                line-height: 96px;

                @media (max-width:955.99px) {
                    font-size: 76px;
                    line-height: 76px;
                }

                @media (max-width:575.99px) {
                    font-size: 56px;
                }

                @media (max-width:479.99px) {
                    font-size: 36px;
                }

            }
        }

        &-btns {
            display: flex;
            align-items: center;
            gap: 24px;
            margin-bottom: 200px;

            @media (max-width:767.99px) {
                margin-bottom: 150px;
            }

            @media (max-width:479.99px) {
                margin-bottom: 20px;
            }
        }
    }
}
</style>