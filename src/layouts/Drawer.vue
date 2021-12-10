<template>
    <q-drawer
      v-model="arbirMenu"
      bordered
      overlay
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>

       
      </q-list>
    </q-drawer>
</template>
<script>
import { defineComponent, inject } from 'vue'

export default defineComponent({
    setup() {
        const arbirMenu = inject('abrirMenu')
        return{
            arbirMenu
        }
    },
})
</script>
