<template>
    <div class="card">
        <img :src="item.imgPath" :alt="item.altName">
        <h4 class="card-title">
            {{ item.name }}
        </h4>
    </div>
</template>

<script setup>
defineProps({
    item: Object
})
</script>

<style lang="scss" scoped>
.card {
    width: 100px;
    height: 110px;
    background: rgba(57, 62, 70, 0.75);
    border-radius: 24px;
    padding: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 5px;

    @media (max-width:901.99px) {
        width: 80px;
        height: 90px;
    }


    @media (max-width:479.99px) {
        font-size: 11px;
        flex-direction: row;
        width: max-content;
        height: max-content;
    }

    & img {
        @media (max-width:901.99px) {
            width: 50px;
            height: 50px;
        }


        @media (max-width:479.99px) {
            width: 15px;
            height: 15px;
        }
    }
}

.card-title {
    color: var(--mainColorText);
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.50);
    font-family: "Poppins";
    font-size: 18px;
    font-weight: 700;
    user-select: none;

    @media (max-width:901.99px) {
        font-size: 16px;
    }

    @media (max-width:400.99px) {
        font-size: 12px;
    }
}
</style>