<template>
  <h1>Contador: {{contador}}</h1>
  <Btn
    :textoBoton="'Aumentar'"
    @accionBtn='aumentar'
  />
  <Btn
    :textoBoton="'Disminuir'"
    @accionBtn='disminuir'
  />
</template>

<script>
import Btn from '../components/Btn.vue'
import { useContador } from '../hooks/useContador'
export default {
  components: {
    Btn
  },
  setup() {
    return {...useContador()}
  }
}
</script>
