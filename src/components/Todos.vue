<template>
  <div>
      <h3>Todos</h3>
      

      <div class="todos">
          <div v-for="todo in allTodos" :key="todo.id" class="todo">
            <b> {{todo.id}}</b>. {{todo.title}}
            <i @click="deleteTodo(todo.id)" class="fa fa-trash" >  </i>
          </div>
      </div>
    
  </div>
</template>

<script>
import {mapGetters, mapActions} from 'vuex';

export default {
    name:'Todos',
    computed:mapGetters(['allTodos']),
    
    methods:{
        ...mapActions(['fetchTodos', 'deleteTodo'])
    },
    created(){
        this.fetchTodos();
    }
}
</script>

<style scoped>
.todos {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 1rem;
}

.todo {
  border: 1px solid #ccc;
  background: #c9e7da;
  padding: 1rem;
  border-radius: 5px;
  text-align: center;
  position: relative;
  cursor: pointer;
}

i{
  position: absolute;
  bottom: 15px;
  right: 10px;
  color: rgb(66, 93, 121);
  cursor: pointer;
}

</style>