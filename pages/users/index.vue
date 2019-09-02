<template>
  <div>
    <!-- binding it to the userId data property -->
    <input type="text" v-model="userId" />
    <button @click="onLoadUser">Load User</button>
  </div>
</template>



<script>
export default {
  data() {
    return {
      userId: ""
    };
  },
  // programmatic navigation for userId input
  methods: {
    onLoadUser() {
      this.$router.push(`/users/${this.userId}`);
    }
  }
};
</script>