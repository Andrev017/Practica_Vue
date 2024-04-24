<script setup>
import { ref, computed } from 'vue'
let id = 0
const newTodo = ref('')
const hideCompleted = ref(false)
const todos = ref([
    { id: id++, text: 'zanahorias', done: true },
    { id: id++, text: '1k de carne', done: true },
    { id: id++, text: 'lehce', done: false }
])
const filteredTodos = computed(() => {
    return hideCompleted.value
        ? todos.value.filter((t) => !t.done)
        : todos.value
})
function addTodo() {
    todos.value.push({ id: id++, text: newTodo.value, done: false })
    newTodo.value = ''
}
function removeTodo(todo) {
    todos.value = todos.value.filter((t) => t !== todo)
}
</script>
<template>

    <div class="bloque">
        <h1>Lista de Compras</h1>
        <form @submit.prevent="addTodo">
            <input v-model="newTodo">
            <button>Agregar</button>
        </form>
        <ul>
        </ul>
        <li v-for="todo in filteredTodos" :key="todo.id">
            <input type="checkbox" v-model="todo.done">
            <span :class="{ done: todo.done }">{{ todo.text }}</span>
            <button @click="removeTodo(todo)">x</button>
        </li>
        <button @click="hideCompleted = !hideCompleted">
            {{ hideCompleted ? 'Mostrar' : 'Ocultar' }}
        </button>
        <br><br>
    </div>
    <hr>
    <br>
</template>

<style>
.done {
    text-decoration: line-through;
    color: aquamarine;
}

.bloque {
    text-align: center;
}
</style>