<template>
  <div class="container">
    <Todos/>
    
  </div>
  
</template>

<script>
import Todos from './components/Todos.vue';

export default {
  name: 'App',
  components: {
    Todos
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
