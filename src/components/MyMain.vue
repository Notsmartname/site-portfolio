<template>
    <main>
        <HeaderContent />
        <SectionAbout />
        <SectionProjects />
        <SectionSkills />
        <SectionContact />
    </main>
</template>

<script setup>
import HeaderContent from '@/components/Header/HeaderContent.vue';
import SectionAbout from '@/components/Main/SectionAbout.vue';
import SectionProjects from '@/components/Main/SectionProjects.vue';
import SectionSkills from '@/components/Main/SectionSkills.vue';
import SectionContact from '@/components/Main/SectionContact.vue';

</script>

<style scoped></style>