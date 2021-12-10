<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <Toolbar/>
      <Drawer/>
    </q-header>
    <q-page-container @click="abrirMenu=false">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import Toolbar from './Toolbar.vue'
import Drawer from './Drawer.vue'
import { defineComponent, ref, provide } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
   Toolbar,
   Drawer
  },

  setup () {
    const abrirMenu = ref(false)
    provide('abrirMenu',abrirMenu)
    return {
     abrirMenu
    }
  }
})
</script>
