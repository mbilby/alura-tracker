<template>
<header>
  <h1>
    <img src="../assets/logo.png" alt="">
  </h1>
  <button class="button" @click="alterarOTema">
    {{textoDoBotao}}
  </button>
</header>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: "BarraLateral",
  emits: ['aoTemaAlterar'],
  data () {
    return {
      modoEscuroAtivo: false
    }
  },
  computed: {
    textoDoBotao () {
      if (this.modoEscuroAtivo) {
        return 'Desativar modo escuro'
      }
      return 'Ativar modo escuro'
    }
  },
  methods: {
    alterarOTema () {
      this.modoEscuroAtivo = !this.modoEscuroAtivo
      this.$emit('aoTemaAlterar', this.modoEscuroAtivo)
    }
  }
})
</script>

<style scoped>
/* Todo o estilo do componente*/
header {
  padding: 1rem;
  background: #0d3b66;
  width: 100%;
  height: 100vh;
  text-align: center;
}

@media only screen and (max-width: 768px) {
  header {
    padding: 2.5rem;
    height: auto;
  }
}
</style>
