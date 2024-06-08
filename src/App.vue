<template>
  <PageTitle />
  <CardList />
  <PageFooter />
</template>

<script>
import PageTitle from './components/PageTitle.vue'
import CardList from './components/CardList.vue'
import PageFooter from './components/PageFooter.vue'

export default {
  name: 'App',
  components: {
    PageTitle,
    CardList,
    PageFooter
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #fafafa;
}
</style>
