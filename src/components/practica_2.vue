<script>
export default {
    data() {
        return {
            titleClass: 'titulo',
            h2Atributo: 'color',
            count: 0
        }
    },
    methods: {
        aumentar() {

            this.count++
        }
    }
}

</script>
<template>
    <h1 :class="titleClass">Titulo en rojo</h1>
    <h2 :atri="h2Atributo">Otro color del atributo</h2>
    <div>
        <h1>Contador: {{ count }}</h1>
        <button v-on:click="aumentar">Incrementar</button>
    </div>
    <hr>
</template>

<style>
.titulo {
    color: red;
}

.color {
    color: #189ec0
}
</style>