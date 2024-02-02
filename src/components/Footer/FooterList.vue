<template>
    <ul class="list">
        <slot></slot>
    </ul>
</template>

<style lang="scss" scoped>
.list {
    display: flex;
    align-items: center;
    gap: 48px;
    margin: 0 auto;

    @media (max-width:479.99px) {}
}
</style>