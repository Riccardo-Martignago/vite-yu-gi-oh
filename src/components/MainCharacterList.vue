<script>
export default {
  data() {
    return {
    }
  },
  props:{
    characters:{
      type: Array,
      required: true
    }
  }
}
</script>

<template>
  <footer>
    CIAO
    <p>
      Number of characters {{ characters.length }}
    </p>
    <ul>
      <li v-for="character in characters" :key="character.id">
        <img :src="character.card_images.image_url_small" :alt="character.name">
        {{ character.name }}
      </li>
    </ul>
  </footer>
</template>

<style lang="scss" scoped>

</style>