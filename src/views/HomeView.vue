<template>
    <MainLayout>
        <Fullstack />
    </MainLayout>
    <Works />
    
    <NewParallex />
    <ToolStack />

    <Contact>
        <Message />
    </Contact>
</template>

<script setup>
import Contact from "../components/Contact.vue";
import Fullstack from "../components/Fullstack.vue";
import NewParallex from "../components/NewParallex.vue";
import MainLayout from "../components/BannerLayout.vue";
import Message from "../components/contact/Message.vue";
import ToolStack from "../components/ToolStack.vue";
import Works from "../components/WorksLayout.vue";
</script>
