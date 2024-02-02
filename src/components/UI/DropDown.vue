<template>
    <div class="dropdown" ref="isDropdown">
        <button class="dropdown__btn" @click="useMenu" :class="{ 'icon-active': isActive }">
            <svg class="dropdown__btn-img" width="40px" height="40px" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"
                fill="">
                <path fill="#fff" fill-rule="evenodd"
                    d="M19 4a1 1 0 01-1 1H2a1 1 0 010-2h16a1 1 0 011 1zm0 6a1 1 0 01-1 1H2a1 1 0 110-2h16a1 1 0 011 1zm-1 7a1 1 0 100-2H2a1 1 0 100 2h16z" />
            </svg>
        </button>
        <transition name="dropdown">
            <ul class="dropdown__list" v-show="dropdown">
                <li v-for="link in links" :key="link.id" :show-img="false" class="dropdown__list-link" @click="useMenu">
                    <a :href="link.path">{{ link.name }}</a>
                </li>
            </ul>
        </transition>
    </div>
</template>

<script setup>

import { ref, onMounted, onBeforeMount } from 'vue';
const props = defineProps({
    links: {
        type: Array,
        required: true,
    }

});

const dropdown = ref(false);
const isDropdown = ref(null);

const isActive = ref(false)

const useMenu = () => {
    if (!dropdown.value) {
        dropdown.value = true;
    } else {
        dropdown.value = false;
    }
    isActive.value = !isActive.value;
}


const closeDropDown = (event) => {
    if (!isDropdown.value.contains(event.target)) {
        dropdown.value = false;
        if (isActive.value == true) {
            isActive.value = false;
        }
    }
}

onMounted(() => {
    window.addEventListener('click', closeDropDown);
});


onBeforeMount(() => {
    window.removeEventListener('click', closeDropDown);
});
</script>

<style lang="scss" scoped>
.dropdown {
    cursor: pointer;
    position: relative;

    &__btn {
        background: #222831;
        border: none;
        transition: .8s ease all;

        &-img {

            @media (max-width:767.99px) {
                height: 35px;
                width: 35px;
            }

            @media (max-width:479.99px) {
                height: 30px;
                width: 30px;
            }
        }
    }

    &__list {
        margin-top: 5px;
        position: absolute;
        left: -27px;

        @media (max-width:1199.99px) {
            left: -20px;
        }

        &-link {
            padding: 10px 0;
            min-width: 100px;
            width: 100%;
            border: 1px solid rgba(238, 238, 238, 0.45);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 8px;
            margin-top: 4px;
            background: #222831;
            transition: .3s;

            @media (max-width:1199.99px) {
                padding: 8px 0;
                min-width: 80px;
                width: 100%;
                border-radius: 6px;
                margin-top: 3px;
            }

            & a {
                color: var(--mainColorText);
                font-family: "Poppins";
                font-size: 18px;
                font-weight: 400;
                display: flex;
                align-items: center;
                gap: 10px;
                transition: .2s;

                @media (max-width:1199.99px) {
                    font-size: 16px;
                    font-weight: 400;
                    gap: 8px;
                }

            }
        }

        &-link:last-of-type {
            border-bottom-left-radius: 8x;
            border-bottom-right-radius: 8px;
        }

        &-link:hover {
            background-color: #414449;
            transform: scale(1.05);

            & a {
                color: var(--subMainColorText);
                transform: scale(1.1);
            }
        }
    }
}


.icon-active {
    transform: rotate(180deg);
}

.dropdown-enter-active {
    transition: all .3s ease-out;
}

.dropdown-leave-active {
    transition: all .3s cubic-bezier(1, .5, .8, 1);
}

.dropdown-enter-from,
.dropdown-leave-to {
    transform: translateY(-8px);
    opacity: 0;
}
</style>