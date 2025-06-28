<script setup>
import TodoItem from './TodoItem.vue';

defineProps(['todos1']);//here todos1 used into app.vue (:todos1="todos" here todos become store input data)

const emit = defineEmits(['toggle-complete2', 'delete-todo2']);
</script>

<template>
  <ul class="list-group w-50 mx-auto">
    <TodoItem v-for="(todo, index) in todos1" :key="index" :todo="todo" :index="index"
      @toggle-complete1="emit('toggle-complete2', index)"
      @delete-todo1="emit('delete-todo2', index)" />
  </ul>
</template>