<script>
import MainCharacterList from './MainCharacterList.vue';
import axios from 'axios';
export default {
  components:{
    MainCharacterList
  },
  data() {
    return {
      characters: [],
    }
  },
  methods:{
    getCharacters(){
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
  .then((response) => {
    console.log(response.data.data);
    this.characters = response.data.data
  })
  .catch(function (error) {
    console.log(error);
  })
  .finally(function () {
  });
    }
  },
  created(){
    this.getCharacters();
  }
}
</script>

<template>
  <main>
    <div class="container">
      <button>Alien</button>
      <div>
        <MainCharacterList :characters="characters" />
      </div>
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
