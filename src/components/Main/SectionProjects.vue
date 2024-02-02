<template>
    <section class="section__bg" id="projects">
        <div class="section__projects">
            <div class="section__projects-text container ">
                <SectionTitle class="section__about-text-title">My <span>Projects</span></SectionTitle>
            </div>
            <div class="section__projects-cards">
                <swiper style="{
      '--swiper-navigation-color': '#fff',
      '--swiper-pagination-color': '#fff',
    }" :zoom="true" :navigation="true" :pagination="{
        clickable: true,
    }" :modules="modules" class="mySwiper">
                    <swiper-slide v-for="project in projects" :key="project.id" class="project__card">
                        <div class="swiper-zoom-container" style="padding: 15px;">
                            <img :src="project.imgPath" style="height: 50%; width: 50%;" />
                            <div class="project__card-skills">
                                <div class="project__card-skills-name" v-for="(skill, index) in project.skill" :key="index">
                                    {{ skill }}
                                </div>
                            </div>
                        </div>
                    </swiper-slide>
                </swiper>
            </div>
        </div>
    </section>
    <LineButton />
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Zoom, Pagination } from 'swiper/modules';
import { ref } from 'vue'
import 'swiper/css';
import 'swiper/css/zoom';
import 'swiper/css/navigation';
import 'swiper/css/pagination';



import SectionTitle from '@/components/UI/SectionTitle.vue';
import LineButton from '@/components/UI/LineButton.vue';
// import ProjectCard from '@/components/UI/ProjectCard.vue';



const projects = [
    { id: 1, skill: ['css', 'html'], imgPath: '/images/projects/1.png' },
    { id: 2, skill: ['css', 'html'], imgPath: '/images/projects/2.png' },
    { id: 3, skill: ['css', 'html'], imgPath: '/images/projects/3.png' },
    { id: 4, skill: ['css', 'html'], imgPath: '/images/projects/4.png' },
    { id: 5, skill: ['css', 'html', 'js'], imgPath: '/images/projects/5.png' },
    { id: 6, skill: ['css', 'html', 'js'], imgPath: '/images/projects/6.png' },
]


const modules = ref([Zoom, Navigation, Pagination]);
</script>

<style lang="scss" scoped>
.project__card {
    position: relative;

    &-skills {
        position: absolute;
        bottom: 20px;
        display: flex;
        align-items: center;
        gap: 5px;
        user-select: none;
        bottom: 35px;

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
}

.section__projects {
    padding-top: 20px;
    padding-bottom: 70px;

    @media (max-width:955.99px) {
        padding: 50px 0;
    }

    &-text {
        display: flex;
        align-items: center;
        gap: 150px;
    }

    &-cards {
        position: relative;
        // margin-top: 40px;
        // display: flex;
        // gap: 25px;
        // width: 100%;
        user-select: none;

        @media (max-width:955.99px) {
            flex-wrap: nowrap;
            overflow-x: scroll;
            gap: 10px;
            height: 550px;


            &::-webkit-scrollbar {
                width: 2px;
                height: 5px;
                border-radius: 3px;
                background: rgba(57, 62, 70, 0.50);
            }

            &::-webkit-scrollbar-thumb {
                width: 5px;
                border-radius: 3px;
                background: var(--seconderyColorText);
            }

            &::-webkit-scrollbar-thumb:active {
                background: #359491;
            }


        }

        @media (max-width:767.99px) {
            height: 100%;
            margin-top: 20px;

        }
    }
}

.section__bg {
    background-image: linear-gradient(#222831fa, rgba(53, 46, 46, 0.1)), url(/images/doodle-items.svg);
    background-repeat: repeat;
    background-size: 30%;
    position: relative;
    background-attachment: fixed;
    z-index: 10;

}


.all-btn {
    max-width: 130px;
}

.swiper {
    padding: 0 100px;
    display: flex;
    gap: 15px;


    &-button-prev,
    &-button-next {
        color: rgb(151, 26, 26);
        background-color: red;
        width: 250px;
        height: 250px;

        &::after {
            font-size: 24px;
            font-weight: 700;
        }
    }
}

.swiper-button-disabled {
    display: none;
}
</style>