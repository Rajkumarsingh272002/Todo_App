<script setup>
import TodoForm from './components/TodoForm.vue';
import {ref} from 'vue';
import TodoList from './components/TodoList.vue';
const todos=ref([])

//add item
const addTodo = (todoText) => {
 console.log('todoText',todoText);
 todos.value.push({ text: todoText.trim(), completed: false });
 console.log(todos.value);  // Logs the updated todos array
}


//toggleComplete2
function toggleComplete2(index2){
console.log("first",todos.value);
console.log("second",todos.value[index2]);
console.log("third",todos.value[index2]);
console.log(todos.value[index2].completed);
todos.value[index2].completed = !todos.value[index2].completed; //true/false
}

//deleteComplete2
function deleteComplete2(index2){
todos.value.splice(index2,1);//remove elemnt from array (const todos=ref([]))
}

</script>

<template>
  <div>
   
  <TodoForm @add-todo="addTodo"/>
  <TodoList :todos1="todos" @toggle-complete2="toggleComplete2" @delete-todo2="deleteComplete2"/><!-- here :todos1 which are props of TodoList.vue-->
  
</div>
  </template>

<style scoped>
</style>