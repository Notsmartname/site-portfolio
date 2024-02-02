<template>
    <swiper-slide class="project__card">
        <img :src="project.imgPath" alt="Project-Img">
        <div class="project__card-skills">
            <div class="project__card-skills-name" v-for="(skill, index) in project.skill" :key="index">
                {{ skill }}
            </div>
        </div>
    </swiper-slide>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
const props = defineProps({
    project: Object,
})


</script>

<style lang="scss" scoped>
.project__card {
    width: 348px;
    background: rgba(57, 62, 70, 0.50);
    backdrop-filter: blur(4px);
    // border-radius: 5%;
    flex: 0 0 auto;
    // overflow: hidden;
    display: flex;
    justify-content: center;
    position: relative;


    cursor: pointer;

    &-skills {
        position: absolute;
        bottom: 20px;
        display: flex;
        align-items: center;
        gap: 5px;
        user-select: none;

        &-name {
            padding: 2px 5px;
            border-radius: 5px;
            background-color: var(--subMainColorText);
            backdrop-filter: blur(4px);
            color: var(--colorBg);
            font-family: "Poppins";
            font-weight: bold;
            font-size: 18px;
            text-transform: uppercase;
            border: 1px solid black;
        }
    }

    & img {
        height: 100%;
        width: 100%;
        background-size: cover;
    }



    @media (max-width:767.99px) {
        height: 500px;
    }
}
</style>