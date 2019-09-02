<template>
  <div>
    <Header />
    <!-- THis is the place where different pages should be loaded in (by using nuxt/) -->
    <nuxt />
  </div>
</template>

<script>
import Header from "~/components/Header";
export default {
  components: {
    Header
  }
};
</script>

<style>
</style>
