<template>
  <div class="container">
    <AddTodo/>
    <FilterTodo/>
    <Todos/>
    
    
  </div>
  
</template>

<script>
import Todos from './components/Todos.vue';
import AddTodo from './components/AddTodo.vue';
import FilterTodo from './components/FilterTodo.vue';
export default {
  name: 'App',
  components: {
    Todos, 
    AddTodo,
    FilterTodo
  }
}
</script>

<style>
/**


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
 */
 body{
   font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
   line-break: 1.6;
   background: whitesmoke;

 }
 .container{
   max-width: 1100px;
   margin: auto;
   overflow: auto;
   padding: 0 2rem;

 }


</style>
