<template>
    <div class="box has-text-weight-bold" :style="estilos">
        <slot></slot>
    </div>
</template>

<script lang="ts">
import { defineComponent, DefineComponent } from 'vue';

export default defineComponent({
    name: "BoxVue",
    data() {
        return{
            estilos:{
                background: '#FAF0CA'
            }
        }
    }
})
</script>
