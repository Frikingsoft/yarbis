<template>
  <div class="titulo">


  <q-toolbar class="animarFondo row items-center justify-between">
    <div class="col-xs-1 col-md-2 botonMenu">
        <q-btn flat dense round icon="menu" aria-label="Menu" @click="abrirMenu=true"/>
    </div>
    <q-toolbar-title class="elTitulo icono row items-center col-12 justify-center">
      Yarbis
      <q-icon
        name="fas fa-laptop-house"
        class="text-white q-ml-md icono"
        style="font-size: 30px"
      />
    </q-toolbar-title>
   
  </q-toolbar>
    </div>
</template>
<script>
import { defineComponent,inject } from "vue";

export default defineComponent({
  setup() {
      
      return{
        abrirMenu:inject('abrirMenu')
      }
  },
});
</script>
<style scoped>
.titulo {
   background-image: linear-gradient(
    to top,
    rgb(13, 71, 108),
    rgb(100, 154, 190)
  );
  
  
  
}
.elTitulo {
  font-size: 40px;
  letter-spacing: 3px;
  text-shadow: 1px 1px 2px black;  
}

.animarFondo{
  background-image: url('../../public/imagenes/fondo.png');
   animation: animar linear 5s infinite;
   background-repeat: repeat;
   background-size: 20% ;
}
.botonMenu{
  position: absolute;
}
.icono{
  text-shadow: 0 0 5px white;
}
@media (max-width: 1023px) {
  
  .elTitulo{
    font-size: 25px;
    letter-spacing: 0;
    word-spacing: 0;
  }
  
}
  @keyframes animar{
        0%{
          background-position: 0 -500px;
        }
        100%{
          background-position: 0 -50px;
        }
      }
</style>