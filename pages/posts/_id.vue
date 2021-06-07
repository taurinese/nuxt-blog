<template>
  <div>
    <Post :post="post" />
  </div>
</template>

<script>
import Post from '../../components/Post.vue'
export default {
  components: { Post },
  async asyncData({ params }) {
    const post = await fetch(
      `https://jsonplaceholder.typicode.com/posts/${params.id}`
    ).then((res) => res.json())
    return { post }
  },
}
</script>

<style scoped></style>
