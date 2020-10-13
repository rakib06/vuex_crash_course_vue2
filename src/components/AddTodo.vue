<template>
  <div>
    <h3> Add Todo </h3>
    <div class="add">
      <form @submit="onSubmit">
        <input type="text" v-model="title" placeholder="Add Todo">
        <input type="submit" value="+">
      </form>
    </div>
  </div>
  
</template>

<script>
import {mapActions } from 'vuex';
export default {
    name: "AddTodo",
    data(){
      return{
        title: ''
      }
    },
    methods : {
      onSubmit(e) {
        e.preventDefault();
        this.addTodo(this.title)
      },
      ...mapActions(['addTodo'])
    }
    
}
</script>

<style scoped>
form {
  display: flex;
}

input[type="text"] {
  flex: 10;
  padding: 10px;
  border: 1px solid #41b883;
  outline: 0;
}

input[type="submit"]{
  flex: 2;
  background: #f6f5f7;
  color: #41b883;
  border:1px solid #e3e2e7;
  cursor: pointer;
}

</style>