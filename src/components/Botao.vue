<template>
  <button class="button" @click="clicado" :disabled="cronometroRodando">
     <span class="icon">
       <i class="fas fa-play"></i>
     </span>
     <span>{{ texto }}</span>
  </button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: "Botao",
  emits: ['clicado'],
  props: {
    desabilitado: {
      type: Boolean
    },
    icone: {
      type: String,
      required: true
    },
    texto: {
      type:String,
      required: true
    },
  },
  methods: {
    clicado () : void {
      this.$emit('clicado')
    }
  } 
  
});
</script>
