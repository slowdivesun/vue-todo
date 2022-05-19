<template>
  <div class="container">
    <HeaderItem/>
    <NewTask/>
  </div>
</template>

<script>
import HeaderItem from './components/HeaderItem'
import NewTask from './components/NewTask.vue'

export default {
  name: 'App',
  components: {
    HeaderItem, NewTask
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
