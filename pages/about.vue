<template>
  <div>
    <div class="flex flex-row justify-center items-center mt-16">
      <div class="w-2/5 h-1/3">
        <img
          class="rounded"
          src="https://media.giphy.com/media/jpbnoe3UIa8TU8LM13/giphy.gif"
          alt=""
        />
      </div>
      <div class="w-2/5 pl-8">
        <h3 class="italic text-4xl mb-4">La crème de Webstart</h3>
        <h1 class="text-8xl uppercase font-bold mb-12">About us</h1>
        <a href="https://media.giphy.com/media/RhrAmVUHxjTQvEPBWi/giphy.gif"
          ><p class="hover:underline">> C'est pas l'âge qui fait le moine</p></a
        >
        <a href="https://media.giphy.com/media/RhrAmVUHxjTQvEPBWi/giphy.gif"
          ><p class="hover:underline">
            > C'est pas au vieux singe qu'on apprend à faire des limaces
          </p></a
        >
        <a href="https://media.giphy.com/media/RhrAmVUHxjTQvEPBWi/giphy.gif"
          ><p class="hover:underline">> Je suis têtue comme une moule</p></a
        >
        <a href="https://media.giphy.com/media/RhrAmVUHxjTQvEPBWi/giphy.gif"
          ><p class="hover:underline">> Tu les emmerdes avec un grand A</p></a
        >
        <a href="https://media.giphy.com/media/RhrAmVUHxjTQvEPBWi/giphy.gif"
          ><p class="hover:underline">> C'est la guerre mondiale de 78</p></a
        >
        <a href="https://media.giphy.com/media/RhrAmVUHxjTQvEPBWi/giphy.gif"
          ><p class="hover:underline">
            > C'est dur d'être filmé 7 jours sur 24
          </p></a
        >
        <a href="https://media.giphy.com/media/RhrAmVUHxjTQvEPBWi/giphy.gif"
          ><p class="hover:underline">> Les oreilles ont des murs</p></a
        >
        <a href="https://media.giphy.com/media/RhrAmVUHxjTQvEPBWi/giphy.gif"
          ><p class="hover:underline">
            > C'est une fille qui n'a pas sa langue dans sa bouche, ça c'est
            clair
          </p></a
        >
        <a href="https://media.giphy.com/media/RhrAmVUHxjTQvEPBWi/giphy.gif"
          ><p class="hover:underline">
            > Je crois que je vais me présenter aux présidentielles de Los
            Angeles
          </p></a
        >
        <a href="https://media.giphy.com/media/RhrAmVUHxjTQvEPBWi/giphy.gif"
          ><p class="hover:underline">
            > Je peux plus me le voir en teinture
          </p></a
        >
        <div
          class="
            w-48
            text-center
            border-2 border-blue-600
            rounded-lg
            px-3
            py-2
            text-blue-400
            cursor-pointer
            hover:bg-blue-600 hover:text-blue-200
            mt-8
          "
          :class="{ disabled: alert }"
          @click.prevent="setAlert()"
        >
          Learn more
        </div>
      </div>
    </div>
    <Alert :message="'Aucune inspi'" @dismiss="dismiss" v-if="alert" />
  </div>
</template>

<script>
import Alert from '../components/Alert.vue'

export default {
  components: { Alert },
  methods: {
    setAlert() {
      this.alert = true
    },
    dismiss() {
      this.alert = false
    },
  },
  data() {
    return {
      alert: false,
    }
  },
}
</script>

<style scoped>
.disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
</style>
