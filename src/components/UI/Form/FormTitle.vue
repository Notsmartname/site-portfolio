<template>
    <label class="title">
        <slot></slot>
    </label>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.title {
    color: var(--mainColorText);
    font-size: 18px;
    font-weight: 700;

    @media (max-width:575.99px) {
        font-size: 15px;
    }

}
</style>