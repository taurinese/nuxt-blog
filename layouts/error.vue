<template>
  <div>
    <div
      v-if="error.statusCode === 404"
      class="error flex flex-col items-center justify-center"
    >
      <img class="w-48 absolute sad-cat" src="~/assets/sadcat.png" alt="" />
      <p class="text-gray-800 w-full text-center text-8xl font-bold">404</p>
      <p class="text-xl">Page not found</p>
    </div>
    <div v-else class="error flex flex-col items-center justify-center">
      <img class="w-48 absolute sad-cat" src="~/assets/sadcat.png" alt="" />
      <p class="text-gray-800 w-full text-center text-8xl font-bold">
        {{ error.statusCode }}
      </p>
      <p class="text-xl">An error occured</p>
    </div>
    <NuxtLink class="hover:bg-gray-200 rounded p-4" to="/"
      >↩️ Go back to home page</NuxtLink
    >
  </div>
</template>

<script>
export default {
  props: ['error'],
  layout: 'error', // you can set a custom layout for the error page
}
</script>
<style scoped>
.error {
  height: calc(100vh - 6.25rem);
}
.sad-cat {
  transform: translate(-53%, -75%);
  left: 50%;
}
</style>
