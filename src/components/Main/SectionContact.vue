<template>
    <section class="section__contact container" id="contact">
        <div class="section__contact-left">
            <SectionTitle class="section__contact-title">Got a project in <span>mind?</span></SectionTitle>
            <div class="section__contact-left-img">
                <img src="/images/man-3.svg" alt="">
            </div>
        </div>
        <div class="section__contact-right">
            <FormVue />
        </div>
    </section>
    <LineButton />
</template>

<script setup>
import LineButton from '@/components/UI/LineButton.vue';
import SectionTitle from '@/components/UI/SectionTitle.vue';

import FormVue from '@/components/UI/Form/FormVue.vue';

</script>

<style lang="scss" scoped>
.section__contact {
    display: flex;
    align-items: center;
    padding: 238px 0;

    @media (max-width:1199.99px) {
        justify-content: center;
        flex-direction: column;
        padding: 140px 0;
        align-items: normal;

    }

    @media (max-width:575.99px) {
        padding: 100px 0;

    }

    &-left {
        display: flex;
        flex-direction: column;
        position: relative;

        @media (max-width:1200.99px) {
            flex-direction: row !important;
            justify-content: center;
            margin-bottom: 50px;
        }

        &-img {
            width: 255px;
            height: 348px;
            margin: 0 auto;
            position: relative;

            @media (max-width:575.99px) {
                display: none;
            }
        }

        &-img::after {
            position: absolute;
            content: '';
            width: 190px;
            height: 24px;
            z-index: -991;
            background-color: rgba(0, 0, 0, 0.50);
            border-radius: 80%;
            right: 80px;
            top: 340px;

        }


    }

    &-left::before {
        position: absolute;
        content: url(../images/arrow-down.svg);
        width: 112px;
        height: 170px;
        top: 220px;
        left: 10px;

        @media (max-width:1200.99px) {
            display: none;
        }


    }

    &-right {
        display: flex;
        flex-direction: column;
        position: relative;
    }

    &-right::before {
        position: absolute;
        content: url(../images/keyboard.svg);
        top: -210px;

        @media (max-width:575.99px) {
            display: none;
        }
    }

    &-right::after {
        position: absolute;
        content: url(../images/mail.svg);
        top: 550px;
        right: 70px;

        @media (max-width:575.99px) {
            display: none;
        }
    }
}
</style>