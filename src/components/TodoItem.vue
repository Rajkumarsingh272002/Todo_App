<script setup>
defineProps(['todo', 'index']);
const emit = defineEmits(['toggle-complete1', 'delete-todo1']);


// Emit toggle complete event with index3
const toggleComplete = () => {
  emit('toggle-complete1', "index3" )// Pass the index3 properly but "index3" no used". you can remove "index3" then also will become work
};

// Emit delete todo event with index
const deleteTodo = () => {
  emit('delete-todo1', "index3"); // Pass the index3 properly "index3" no used. you can remove "index3" then also will become work
};
</script>

<template>
  <li class="list-group-item d-flex justify-content-between">
    <span :class="{ 'text-decoration-line-through': todo.completed }">{{ todo.text }}</span>
    <div>
      <button @click="toggleComplete" class="btn btn-sm btn-success me-2">✔</button>
      <button @click="deleteTodo" class="btn btn-sm btn-danger">🗑</button>
    </div>
  </li>
</template>
