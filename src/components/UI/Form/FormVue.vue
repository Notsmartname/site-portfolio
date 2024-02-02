<template>
    <form action="#" class="form">
        <div class="form__header">
            <FormColumn>
                <FormTitle for="name">Your name:</FormTitle>
                <FormInput placeholder="Name" id="name" />
            </FormColumn>
            <FormColumn>
                <FormTitle for="email">Your email:</FormTitle>
                <FormInput placeholder="Email" id="email" />
            </FormColumn>
        </div>
        <div class="form__body">
            <FormColumn class="textarea">
                <FormTitle for="message">Your Message</FormTitle>
                <FormTextarea name="message" id="message" placeholder="Message" />
            </FormColumn>
            <WhiteBtn href="#">Send Message
                <img src="/images/send.svg" alt="send" v-if="screenWidth > 419.99">
            </WhiteBtn>
        </div>
    </form>
</template>

<script setup>
import { ref } from 'vue';
import FormInput from '@/components/UI/Form/FormInput.vue';
import FormTitle from '@/components/UI/Form/FormTitle.vue';
import FormColumn from '@/components/UI/Form/FormColumn.vue';
import FormTextarea from '@/components/UI/Form/FormTextarea.vue';
import WhiteBtn from '@/components/UI/WhiteBtn.vue';

const screenWidth = ref(window.innerWidth);
window.addEventListener('resize', () => {
    screenWidth.value = window.innerWidth;
})
</script>

<style lang="scss" scoped>
.form__header {
    display: flex;
    align-items: center;
    gap: 24px;

    @media (max-width:419.99px) {
        flex-direction: column;
        align-items: normal;
    }
}

.form__body {
    margin-top: 24px;
    display: flex;
    flex-direction: column;
    gap: 24px;
}

.textarea {
    @media (max-width:419.99px) {
        flex-direction: column;
        align-items: normal;
    }
}
</style>