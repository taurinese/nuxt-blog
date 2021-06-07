<template>
  <div class="my-24 relative">
    <img
      src="https://media.giphy.com/media/Oj7cKjOoBwNnYcMY4p/giphy.gif"
      alt=""
      class="rodeo-running"
    />
    <div class="rodeo-running block-running"></div>
    <h1 class="text-center text-4xl mb-8">{{ post.title }}</h1>
    <p class="px-8">{{ post.body }}</p>
  </div>
</template>

<script>
export default {
  props: ['post'],
}
</script>

<style scoped>
.rodeo-running {
  position: absolute;
  left: 0;
  top: -150%;
  animation: running 2s;
  animation-fill-mode: forwards;
  z-index: 99;
  transform: scaleX(-1);
}
.block-running {
  background-color: white;
  top: -50%;
  width: 100%;
  height: 200px;
  content: '';
  z-index: 5;
}

@keyframes running {
  from {
    left: 0;
  }
  to {
    left: 100%;
  }
}
</style>
