<template>
  <div>
    <!-- binding it to the userId data property -->
    <input type="text" v-model="userId" />
    <button @click="onLoadUser">Load User</button>
    <!-- this loads all the children inside users folder including index.js -->
    <nuxt-child />
  </div>
</template>



<script>
export default {
  data() {
    return {
      userId: ""
    };
  },
  methods: {
    onLoadUser() {
      // programmatic navigation for userId input
      this.$router.push(`/users/${this.userId}`);
    }
  },
  // this is special property understood by nuxt to be used for styling this component (inside layout folder)
  layout: "users"
};
</script>