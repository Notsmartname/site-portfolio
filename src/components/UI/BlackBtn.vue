<template>
    <a href="#" class="btn right-btn">
        Download CV
    </a>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.btn {
    display: flex;
    padding: 10px 32px;
    align-items: center;
    gap: 10px;
    color: var(--mainColorText);
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.50);
    font-family: "Poppins";
    font-size: 18px;
    font-weight: 700;
    user-select: none;
    border-radius: 24px;
    background: rgba(57, 62, 70, 0.75);
    backdrop-filter: blur(2px);
    max-width: 223px;
    justify-content: center;

    @media (max-width:955.99px) {
        font-size: 16px;
        max-width: 200px;
    }

    @media (max-width:575.99px) {
        padding: 5px 10px;
    }

    @media (max-width:479.99px) {
        padding: 4px 10px;
    }


}
</style>