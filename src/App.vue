<template>
  <div class="container">
    <form v-if="username===null" @submit="(e)=>onSubmit(e)">
      <input @change="(e)=>onChange(e)" type="text" :value="username"/>
      <button type="submit">Submit Username</button>
    </form>
    <h1 class="username" v-if="username!==null">{{username}}</h1>
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
  },
  data(){
    return {
      userPresent: false,
      input: "",
      username: null,
      tasks: []
    }
  }, 
  methods: {
    onSubmit(e){
      e.preventDefault();
      this.userPresent = true;
      this.username = this.input;
      console.log(this.username)
    },
    onChange(e){
      this.input = e.target.value
    }
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

.btn{
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    background: black;
    margin: 3px;
}
</style>
