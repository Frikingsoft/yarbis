<template>
  <q-card class="my-card">
    <q-card-section class="fondo-texto text-white text-center col-12">
      <div class="text-h6 texto">Conexiones</div>
    </q-card-section>

    <q-card-section class="col-12 flex justify-end">
      <q-btn push class="botones text-white q-mr-md" @click="agregar = true"> Agregar
          <q-icon
            name="fas fa-user-plus"
            class="q-ml-md icono"
            style="font-size: 20px"
          />
      </q-btn>
      <q-btn push class="botones text-white">Borrar 
        <q-icon
          name="fas fa-trash"
          class="q-ml-md icono"
          style="font-size: 20px"
        />
      </q-btn>
    </q-card-section>
    <q-separator />
    <Agregar/>
  </q-card>
  
</template>
<script>
import Agregar from './Agregar.vue'
import { defineComponent,ref, provide } from 'vue'

export default defineComponent({
   components:{
    Agregar
  },
 setup() {
    const agregar = ref(false)
    provide('agregar',agregar)
    return{
       agregar,
    }
  },
})
</script>

<style scoped>
.fondo-texto {
  background: linear-gradient(to top, rgb(13, 71, 108), rgb(100, 154, 190));
  box-shadow: 1px 1px 6px black;
  height: 60px;
}
.texto {
  letter-spacing: 3px;
  text-shadow: 1px 1px 2px black;
  font-size: 30px;
}
.botones{
   background: linear-gradient(
    to top,
    rgb(13, 71, 108),
    rgb(100, 154, 190)
  );
  letter-spacing: 3px;
  text-shadow: 1px 1px 2px black;
}
</style>