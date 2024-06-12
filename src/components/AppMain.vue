<script>
import MainCharacterList from './MainCharacterList.vue';
export default {
  components:{
    MainCharacterList
  },
  data() {
    return {
    }
  }
}
</script>

<template>
  <main>
    <div class="container">
      <button>Alien</button>
      <div>
        <MainCharacterList />
      </div>
      <h1>MAIN!</h1>
    </div>
  </main>
</template>

<style lang="scss" scoped>
main{
  background-color: #d48f38;
}
.container{
  max-width: 1200px;
  margin: 0 auto;
  div{
    background-color: white;
  }
}
button{
  padding: .3rem .5rem;
  margin: 1rem;
}
</style>
