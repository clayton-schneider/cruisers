<template>
  <div class="layout">
    <Header class="container" :home="false" />
    <slot />
    <Footer class="container" :home="false" />
  </div>
</template>

<script>
import Header from '~/components/Header';
import Footer from '~/components/Footer';
export default {
  components: {
    Footer,
    Header,
  },
};
</script>

<style></style>
