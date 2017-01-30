<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <!--<hello></hello>-->
    <todos :todos="todos"></todos>
    <todo-form :todos="todos"></todo-form>
  </div>
</template>

<script>
  import Hello from './components/Hello'
  import Todos from './components/Todos'
  import TodoForm from './components/TodoForm'

  export default {
    name: 'app',
    data() {
      return {
        message: 'Hello World',
        todos:[
          {id:1,title:'vue',completed:false},
          {id:2,title:'javascript',completed:false}
        ]
      }
    },
    computed: {
      todoCount() {
        return this.todos.length;
      }
    },
    components: {
      Hello,Todos,TodoForm
    }
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
