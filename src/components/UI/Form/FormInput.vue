<template>
    <input type="text" class="input">
</template>

<style scoped lang="scss">
.input {
    display: flex;
    padding: 16px 0 16px 24px;
    align-items: flex-start;
    gap: 10px;
    align-self: stretch;
    border-radius: 16px;
    background: rgba(57, 62, 70, 0.50);
    border: none;
    width: 262px;

    @media (max-width:1226.99px) {
        width: 232px;
    }

    @media (max-width:575.99px) {
        width: 180px;
        padding: 10px 0 10px 18px;

    }

}

.input::placeholder {
    color: var(--primaryColorText);
    font-size: 18px;
    font-weight: 700;

    @media (max-width:575.99px) {
        font-size: 15px;
    }
}

.input:focus {
    outline: none;
}
</style>