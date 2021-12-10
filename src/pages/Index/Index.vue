<template>
  <q-page class="row justify-center q-mt-xl">
    <Conexiones class="col-4"/>
    <Subscripciones class="col-4 q-ml-xl"/>
  </q-page>
</template>

<script>
import Conexiones from './Conexiones/Conexiones.vue'
import Subscripciones from './Subscripciones.vue'
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PageIndex',
  components:{
    Conexiones,
    Subscripciones
  }
})
</script>
