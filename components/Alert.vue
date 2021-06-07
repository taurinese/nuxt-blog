<template>
  <div
    class="
      absolute
      w-48
      h-12
      bg-gray-700
      rounded
      flex
      justify-center
      items-center
      text-white
    "
  >
    {{ message }}
    <img
      class="close cursor-pointer"
      src="~/assets/cancel.svg"
      alt="cancel"
      @click.prevent="$emit('dismiss')"
    />
  </div>
</template>

<script>
export default {
  props: ['message'],
}
</script>

<style scoped>
div {
  top: 5px;
  left: 50%;
  transform: translate(-50%, 0);
}
.close {
  position: absolute;
  top: 8px;
  right: 8px;
  width: 16px;
  height: 16px;
  filter: invert(1);
}
</style>
