<script>
export default {
    data() {
        return {
            text: "",
            count: 10
        }
    },
    methods: {
        aumentar() {

            this.count--
        }
    }
}
</script>

<template>
    <h1>Contador: {{ count }}</h1>
    <button v-on:click="aumentar">Decrementar</button>
    <hr>

    <input v-model="text" placeholder="Escribir">
    <p>{{ text }}</p>
    <br>
    <hr>
    <input pattern="week" name="codigopostal" id="codigopostal" placeholder="AQUIIIIIII">
    

</template>