<template>
    <MainLayout>
        <Fullstack />
    </MainLayout>
    <AboutLayout />
    <Works />
    <ToolStack />

    <Contact>
        <SocialMedia />
        <Message />
    </Contact>
</template>

<script setup>
import AboutLayout from "../components/AboutLayout.vue";
import Contact from "../components/Contact.vue";
import Fullstack from "../components/Fullstack.vue";
import MainLayout from "../components/BannerLayout.vue";
import Message from "../components/contact/Message.vue";
import ToolStack from "../components/ToolStack.vue";
import SocialMedia from "../components/contact/SocialMedia.vue";
import Works from "../components/WorksLayout.vue";
</script>
