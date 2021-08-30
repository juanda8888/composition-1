<template>
  <!-- <h1>Detalle: {{$route.params.nombre}}</h1> -->
  <h1>Detalle: {{nombre}}</h1>
  <p
    v-for="(pais, index) in arrayData"
    :key="index"  
  >
    {{pais.name}} - {{pais.region}}
  </p>
</template>

<script>
import { useFetch } from '../hooks/useFetch'
import { useRoute } from 'vue-router'
export default {
    props: ['nombre'],
    setup(props) {
        const nombreParams = useRoute()
        // console.log(nombreParams.params.nombre)

        return {...useFetch(`https://restcountries.eu/rest/v2/name/${nombreParams.params.nombre}`)}
    }
}
</script>
