<script setup>
import { ref } from 'vue'
// give each todo a unique id
//el reconocimiento de rotro darle funcion, reconocimiento por cara
let id = 0
const newTodo = ref('')
const todos = ref([
    { id: id++, text: 'Learn HTML' },
    { id: id++, text: 'Learn JavaScript' },
    { id: id++, text: 'Learn Vue' }
])
function addTodo() {
    todos.value.push({ id: id++, text: newTodo.value })
    newTodo.value = ''
}
function removeTodo(todo) {
    todos.value = todos.value.filter((t) => t !== todo)
}
</script>
<template>
    <form @submit.prevent="addTodo">
        <input v-model="newTodo">
        <button>Agregar</button>
    </form>
    <ul>
        <li v-for="todo in todos" :key="todo.id">
            {{ todo.text }}
            <button @click="removeTodo(todo)">x</button>
        </li>
    </ul>
    <br>
    <hr>
    
</template>