<template>
    <section class="section__about container" id="about">
        <div class="section__about-text">
            <SectionTitle class="section__about-text-title">About <span>me</span></SectionTitle>
            <p class="section__about-text-descr">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo nulla dolor temporibus, mollitia et ad! Fugit,
                quo. Aliquid praesentium, alias nesciunt repellendus repudiandae tempora magnam? Sint beatae quam dolore
                totam?
            </p>
        </div>
        <div class="section__about-img">
            <img src="/images/doodle-items.svg" alt="Doodle">
        </div>
    </section>
    <LineButton />
</template>

<script setup>
import SectionTitle from '@/components/UI/SectionTitle.vue';
import LineButton from '@/components/UI/LineButton.vue';

</script>


<style lang="scss" scoped>
.section__about {
    padding-top: 196px;
    display: flex;
    gap: 120px;
    padding-bottom: 145px;

    @media (max-width:1199.99px) {
        filter: brightness(.9);
        gap: 20px;
    }

    @media (max-width:1049.99px) {
        position: relative;
        z-index: 1;
        gap: 10px;
        padding-top: 126px;
        padding-bottom: 225px;

    }

    @media (max-width:955.99px) {
        align-items: center;
        justify-content: center;
        padding-top: 106px;
        padding-bottom: 205px;
    }

    @media (max-width:479.99px) {
        padding-top: 50px;
        padding-bottom: 55px;
    }

    @media (max-width:319.99px) {}

    &-img {
        position: relative;
        z-index: -99;

        @media (max-width:1049.99px) {
            max-width: 800px;
            position: absolute;
            filter: brightness(.9);
            display: flex;
            align-self: center;
            justify-content: center;

        }

        & img {
            filter: brightness(.5);
            z-index: 0;

            @media (max-width:1225.99px) {
                max-width: 900px;
                width: 100%;

            }

            @media (max-width:1199.99px) {
                max-width: 1000px;
                width: 100%;

            }

            @media (max-width:955.99px) {
                z-index: -100;
                max-width: 800px;

            }

            @media (max-width:479.99px) {
                z-index: -100;
                max-width: 250px;

            }
        }


    }

    &-img::after {
        position: absolute;
        content: '';
        width: 348px;
        height: 24px;
        border-radius: 80%;
        background: rgba(0, 0, 0, 0.50);
        bottom: -90px;
        left: 50%;
        transform: translate(-50%, -50%);
        z-index: 1;
        filter: brightness(.8);

        @media (max-width:1199.99px) {
            position: static;
            width: 0px;
            height: 0px;

        }


    }

    &-img::before {
        filter: brightness(.8);
        z-index: 2;
        position: absolute;

        content: '';
        width: 413px;
        height: 465px;
        border-radius: 80%;
        background: url(/images/man-2.svg);
        background-position: center;
        background-repeat: no-repeat;
        bottom: -355px;
        left: 50%;
        transform: translate(-50%, -50%);

        @media (max-width:1199.99px) {
            position: static;
            width: 0px;
            height: 0px;

        }

        @media (max-width:955.99px) {
            position: static;
            width: 0px;
            height: 0px;
        }
    }

    &-text {
        &-descr {
            width: 389px;
            color: var(--seconderyColorText);
            font-family: "Poppins";
            font-size: 18px;
            font-weight: 400;
            position: relative;

            @media (max-width:955.99px) {
                font-size: 14px;
                width: 340px;
            }

            @media (max-width:400.99px) {
                width: 280px;
                font-size: 10px;
            }

            @media (max-width:319.99px) {
                width: 240px;
            }
        }

        &-descr::after {
            position: absolute;
            width: 113px;
            height: 170px;
            content: '';
            background-image: url(/images/arrow-button.svg);
            background-repeat: no-repeat;
            background-position: center;
            top: 140px;
            left: 168px;

            @media (max-width:1199.99px) {
                top: 100px;
            }

            @media (max-width:955.99px) {
                position: static;
                width: 0px;
                height: 0px;
            }
        }

        &-title {
            position: relative;
            margin-bottom: 15px;
            margin-top: 60px;
        }

        &-title::after {
            position: absolute;
            width: 58px;
            height: 88px;
            right: -10px;
            top: -20px;
            content: '';
            background-image: url(/images/lightbulb.svg);
            background-repeat: no-repeat;
            background-position: center;

            @media (max-width:955.99px) {
                position: static;
                width: 0px;
                height: 0px;
            }
        }

        &-title::before {
            position: absolute;
            width: 62px;
            height: 47px;
            content: '';
            top: -104px;
            background-image: url(images/melody.svg);
            background-repeat: no-repeat;
            background-position: center;

            @media (max-width:955.99px) {
                position: static;
                width: 0px;
                height: 0px;
            }
        }
    }


}
</style>