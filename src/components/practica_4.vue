<script>
export default {
    data() {
        return {
            nombre: '',
            apellido: ''
        }
    }
}
</script>
<template>
    <br>
    <input v-model="nombre" placeholder="Nombre">
    <input v-model="apellido" placeholder="Apellido">

    <p>{{ nombre + apellido }}</p>
    <br>
    <hr>

</template>