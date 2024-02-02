<template>
    <section class="section__skills container" id="skills">
        <div class="section__skills-preview">
            <SectionTitle class="section__skills-preview-title">All My <span>Skills</span></SectionTitle>
            <h2 class=" title">

            </h2>
        </div>
        <div class="section__skills-titles">
            <SkillCard v-for="(item, index) in skillCards" :key="index" :item="item" />
        </div>
    </section>
    <LineButton />
</template>

<script setup>
import SectionTitle from '@/components/UI/SectionTitle.vue';
import LineButton from '@/components/UI/LineButton.vue';
import SkillCard from '@/components/UI/SkillCard.vue';

const skillCards = [
    { name: 'HTML', imgPath: '/images/html-logo.svg', altName: 'HTML' },
    { name: 'Vue', imgPath: '/images/vue-logo.svg', altName: 'Vue' },
    { name: 'CSS', imgPath: '/images/css-logo.svg', altName: 'CSS' },
    { name: 'JavaScript', imgPath: '/images/logo-javascript.svg', altName: 'JavaScript' },
    { name: 'GitHub', imgPath: '/images/github-icon.svg', altName: 'GitHub' },
]

</script>

<style lang="scss" scoped>
.section__skills {
    padding-top: 140px;
    display: flex;
    gap: 300px;
    padding-bottom: 180px;

    @media (max-width:1070.99px) {
        padding-top: 100px;
        gap: 100px;
        padding-bottom: 100px;
    }

    @media (max-width:901.99px) {
        align-items: center;
        gap: 30px;
        justify-content: center;
        flex-direction: column;
    }

    &-preview {
        position: relative;

        &-title {
            position: relative;
        }

        &-title::after {
            position: absolute;
            content: '';
            top: -50px;
            right: -250px;
            width: 70px;
            height: 57px;
            background-image: url(/images/macbook.svg);
            background-repeat: no-repeat;
            transform: rotate(14.817deg);

            @media (max-width:765.99px) {
                right: -50px;
                z-index: -99;

            }
        }

        &-title::before {
            position: absolute;
            content: '';
            top: 220px;
            right: 350px;
            width: 60px;
            height: 45px;
            background-image: url(/images/food.svg);
            background-repeat: no-repeat;
            transform: rotate(14.817deg);

            @media (max-width:765.99px) {
                right: 250px;
                top: 320px;
                z-index: -99;

            }
        }

    }

    &-preview::after {
        position: absolute;
        content: '';
        top: 90px;
        left: 50px;
        width: 290px;
        height: 342px;
        background-image: url(/images/man-1.svg);
        overflow: hidden;

        @media (max-width:901.99px) {
            position: static;
            width: 0px;
            height: 0px;
        }


    }

    &-titles {
        margin-top: 50px;
        display: flex;
        gap: 25px;
        flex-wrap: wrap;
        width: 400px;
        align-items: center;
        justify-content: center;

        @media (max-width:901.99px) {
            width: 350px;
        }

        @media (max-width:479.99px) {
            width: 240px;
            margin-top: 0px;
            gap: 15px;
        }
    }
}
</style>