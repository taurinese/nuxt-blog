<template>
  <div>
    <nav class="w-full flex justify-evenly shadow p-4 text-xl">
      <nuxt-link class="hover:underline" to="/">Home</nuxt-link>
      <nuxt-link class="hover:underline" to="/about">About</nuxt-link>
      <nuxt-link class="hover:underline" to="/posts">Posts</nuxt-link>
    </nav>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
nav {
  z-index: 9999;
}
</style>
