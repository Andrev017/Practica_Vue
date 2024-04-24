<template>
  <pract1 msg="practica n°1 de Vuejs"/>
  <pract2 msg="practica n°2 de Vuejs"/>
  <pract3 msg="practica n°3 de Vuejs"/>
  <pract4 msg="practica n°4 de Vuejs"/>
  <pract5 msg="practica n°5 de Vuejs"/>
  <pract6 msg="practica n°6 de Vuejs"/>
  <pract7 msg="practica n°7 de Vuejs"/>



</template>

<script>
import pract1 from './components/practica_1.vue'
import pract2 from './components/practica_2.vue'
import pract3 from './components/practica_3.vue'
import pract4 from './components/practica_4.vue'
import pract5 from './components/practica_5.vue'
import pract6 from './components/practica_6.vue'
import pract7 from './components/practica_7.vue'


export default {
  name: 'App',
  components: {
    pract1,
    pract2,
    pract3,
    pract4,
    pract5,
    pract6,
    pract7
  }
}
</script>

<style>

</style>
