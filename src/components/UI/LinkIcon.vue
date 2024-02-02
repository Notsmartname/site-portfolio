<template>
    <li>
        <a class="icon">
            <img :src="item.imgPath" :alt="item.altName" />
        </a>
    </li>
</template>

<script setup>
defineProps({
    item: Object
})
</script>

<style lang="scss" scoped>
.icon {
    display: flex;
    width: 48px;
    height: 48px;
    padding: 12px;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    background: #393e46;
    cursor: pointer;

    @media (max-width:479.99px) {
        width: 30px;
        height: 30px;

        & img {
            height: 15px;
            width: 15px;
        }
    }
}
</style>