<template>
  <div class="home">
    <h1>Contador: {{contador}}</h1>
    <button
      class="btn btn-primary"
      @click="aumentar"
    >
      Aumentar
    </button>
    <button
      class="btn btn-orange"
      @click="disminuir"
    >
      Disminuir
    </button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    aumentar() {
      this.contador ++
    },
    disminuir() {
      this.contador --
    }
  }
}
</script>
