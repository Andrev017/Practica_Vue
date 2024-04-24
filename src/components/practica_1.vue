<template>
  <h1>{{ message }}</h1>
  <button>Count is: {{ counter.count }}</button>
  <br>
  <p v-bind:id="mensajeId">Este es un párrafo dinámico</p>
  
  <h1 v-bind:id="{calss}">Titulo dinamico</h1>
  <hr>
</template>

<script>
export default {
  data() {
    return {
      message: 'funciones de vue',
      counter: {
        count: 0
      }
    }
  }
}
</script>


<style scoped></style>
