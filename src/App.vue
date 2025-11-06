<script setup>
import Nav from './components/Nav.vue';
import Page from './components/Page.vue';
import Footer from './components/Footer.vue';
import 'aos/dist/aos.css';
import AOS from 'aos';
AOS.init();
</script>

<template>
    <Nav />
    <Page />
    <Footer />
</template>
