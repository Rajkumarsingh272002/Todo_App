<script setup>
import { ref } from 'vue';

const newTodo = ref('');
const emit = defineEmits(['add-todo']);

const addTodo = () => {
  if (newTodo.value.trim()) {
    emit('add-todo', newTodo.value);
    newTodo.value = ''; // Clear the input after adding the todo
  }
};
</script>

<template>
  <div class="d-flex justify-content-center my-3">
    <input 
      v-model="newTodo" 
      @keyup.enter="addTodo" 
      class="form-control w-50 me-2" 
      placeholder="नया टास्क लिखें"
    />
    <button @click="addTodo" class="btn btn-primary">➕ जोड़ें</button>
  </div>
</template>
