<template>
    <q-card class="my-card row justify-center">
        <q-card-section class="col-6">
             <q-input v-model="datos.valor" :label="datos.nombre" 
             v-for="(datos,index) in datosServidor" :key="index"/>            
        </q-card-section>
    </q-card>
</template>
<script>
import { defineComponent, inject, ref } from 'vue';

export default defineComponent({
    setup() {
        const agregar = inject('agregar')
        const datosServidor = ref([
            {nombre:'Broker',valor:''},
            {nombre:'Ip',valor:''},
            {nombre:'Usuario',valor:''},
            {nombre:'Contraseña',valor:''}
        ])
        return{
            agregar,
            datosServidor
        }
    },
})
</script>
