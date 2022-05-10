<template>
<div class="box has-text-weight-bold" :style="estilos">
    <slot></slot>
</div>
  
</template>

<script>
import { defineComponent } from 'vue'


export default defineComponent({
name: 'Box',
data () {
  return {
    estilos: {
      backgroundColor: '#FAF0CA'
    }
  }
},  
})
</script>


<style scoped>
/*.box {
  background: #FAF0CA;
}*/
</style>