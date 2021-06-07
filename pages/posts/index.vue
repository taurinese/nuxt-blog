<template>
  <div>
    <div class="ml-8 italic">Liste de posts:</div>
    <ul>
      <li v-for="post in posts" :key="post" class="w-screen text-center m-4">
        <nuxt-link
          class="hover:bg-gray-500 hover:text-white p-4 rounded hover:underline"
          :to="`/posts/${post.id}`"
          >{{ post.title }}</nuxt-link
        >
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData() {
    const posts = await fetch(
      'https://jsonplaceholder.typicode.com/posts'
    ).then((res) => res.json())
    return { posts }
  },
}
</script>

<style scoped></style>
