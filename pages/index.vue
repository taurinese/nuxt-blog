<template>
  <div class="container">
    <div>
      <img src="https://i.gifer.com/6kg.gif" alt="" />
      <h1 class="title">Choisis entre</h1>
      <div class="links">
        <nuxt-link to="/error" class="button--green"> Le banger </nuxt-link>
        <nuxt-link to="/about" class="button--grey"> Le classique </nuxt-link>
        <nuxt-link to="/posts/1" class="button--grey">La surprise</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Blog',
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        hid: 'description',
        name: 'description',
        content: 'devoir nuxt - blog',
      },
    ],
  },
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
