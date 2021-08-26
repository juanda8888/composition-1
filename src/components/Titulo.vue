<template>
  <h1
    :style="{'color': color}"
  >
    contador {{signoPeso}}
  </h1>
</template>

<script>
import { computed } from '@vue/reactivity'
export default {
    props: ['color', 'contador'],

    setup(props) {
        const signoPeso = computed(() => {
            return '$ ' + props.contador
        })

        return {signoPeso}
    }
}
</script>
