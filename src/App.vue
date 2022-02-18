<script setup>
import IntroTitle from './components/IntroTitle.vue';
import Form from './components/Form.vue';
import Footer from './components/Footer.vue';
import Nav from './components/Nav.vue';
</script>

<template>
  <div class="container mx-auto px-5">
    <Nav />
    <IntroTitle />
    <Form />
    <Footer />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
};
</script>
