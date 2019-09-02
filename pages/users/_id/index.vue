<template>
  <!-- $route is provided by vue js by the vue router giving us the information with the currently loaded route -->
  <div>This is single user route for : {{$route.params.id}}</div>
</template>
<script>
export default {
  // special methods nuxt js executes

  validate(data) {
    console.log(data);
    // this returns true for number params
    return /^\d+$/.test(data.params.id);
  }
};
</script>