<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HelloWorld from './components/HelloWorld.vue';
import IntroTitle from './components/IntroTitle.vue';
import Form from './components/Form.vue';
import Footer from './components/Footer.vue';
import Nav from './components/Nav.vue';
</script>

<template>
  <div>
    <!-- <HelloWorld msg="Hello Vue 3 + Vite" /> -->

    <div class="container mx-auto px-5">
      <Nav />
      <IntroTitle />
      <Form />
      <Footer />
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
};
</script>

<style></style>
