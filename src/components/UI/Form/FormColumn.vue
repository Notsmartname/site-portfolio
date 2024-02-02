<template>
    <div class="column">
        <slot></slot>
    </div>
</template>

<style lang="scss" scoped>
.column {
    display: flex;
    flex-direction: column;
    gap: 10px;

    @media (max-width:419.99px) {
        flex-direction: row;
        gap: 5px;
        align-items: center;

    }
}
</style>