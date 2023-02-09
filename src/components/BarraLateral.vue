<template>
    <header>
        <h1>
            <img src="data:image/png;base64,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">
        </h1>
        <button class="button" @click="alterarTema">
          {{textoBotao}}
        </button>
    </header>
</template>
 
<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'BarraLateral',
    emits: ['aoTemaAlterado'],
    data () {
      return {
        modoEscuroAtivo: false
      }
    },
    computed: {
      textoBotao() {
        if(this.modoEscuroAtivo) {
          return 'Light Mode'
        }
        return 'Dark Mode'
      }
    },
    methods:{
      alterarTema () {
        this.modoEscuroAtivo = !this.modoEscuroAtivo
        this.$emit('aoTemaAlterado', this.modoEscuroAtivo)
      }
    }
})
</script>


<style scoped>
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