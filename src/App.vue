<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components:{
    AppHeader,
    AppMain,
    AppFooter
  },
  data() {
    return {
    }
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
  @use'./styles/partials/variables' as *;
  @use'./styles/partials/mixins' as *;
  @use'./styles/general.scss';
</style>
