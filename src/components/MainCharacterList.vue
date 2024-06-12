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
        <img :src="character.card_images[0].image_url_small" :alt="character.name">
        <div>
          <h2>{{ character.name }}</h2>
          <p>{{ character.type }}</p>
        </div>
      </li>
    </ul>
  </footer>
</template>

<style lang="scss" scoped>
ul{
  display: flex;
  flex-wrap: wrap;
  padding: 2rem;
  justify-content: space-between;
}
li{
  max-width: calc(100% /5 - 1rem);
  padding-bottom: 1rem;
}
h2{
  color: white;
}
p{
  padding-top: 1rem;
}
div{
  background-color: #d48f38;
  text-align: center;
}
</style>