<template>
    <h2 class="title">
        <slot></slot>
    </h2>
</template>
<script setup>

</script>
<style lang="scss">
.title {
    color: var(--mainColorText);
    font-family: "Poppins";
    font-size: 64px;
    font-weight: 700;
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.50);

    @media (max-width:955.99px) {
        font-size: 46px;
    }

    @media (max-width:479.99px) {
        font-size: 36px;
    }

    @media (max-width:319.99px) {}

    & span {
        color: var(--subMainColorText);

        @media (max-width:479.99px) {
            font-size: 36px;
        }

        @media (max-width:319.99px) {}
    }
}
</style>