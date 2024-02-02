<template>
    <textarea cols="30" rows="10" class="message"></textarea>
</template>

<style lang="scss" scoped>
.message {
    color: rgba(238, 238, 238, 0.50);
    font-size: 18px;
    font-weight: 700;
    border-radius: 16px;
    background: rgba(57, 62, 70, 0.50);
    display: flex;
    height: 280px;
    padding: 16px 24px;
    align-items: flex-start;
    gap: 10px;
    align-self: stretch;
    outline: none;
    border: none;
    resize: none;

    @media (max-width:575.99px) {
        font-size: 15px;
    }
}
</style>

