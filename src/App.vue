<template>
   
     <div class="logoytext">
            <div class="logotextomovil">
                  <img id="logo" src="../src/assets/logok.webp" alt="Logo de Kubiotec">   
            </div>
      
            <div class="button-group">
            <button class="botonContenido" @click="cambiarContenido('HolaKubyhe')" >Inicio</button>
            <button class="botonContenido" @click="cambiarContenido('FabKubyhe')"  >Elaboración</button>
            <button class="botonContenido" @click="cambiarContenido('OMVKubyhe')"  >Nuestra Esencia</button>
            <button class="botonContenido" @click="cambiarContenido('ProductoK')"  >Productos</button>
            <button class="botonContenido" @click="cambiarContenido('contactoK')"  >Contacto</button>
            </div>
            
      </div> <br>


      <div class="content-display">
        <transition name="fade" mode="out-in">
          <component :is="componenteActual"></component>
        </transition>
      </div>


    <br><br>
    <footer>
      <div class="fologoytext">
            <div class="">
                  <p class="fologotext">KubyHe &reg; 2025 ©  ⚡ by <a href="http://wa.me/522281362858" target="_blank"> Kubiotec</a> 📲</p>  
            </div>  
      </div>
    </footer>
</template>

<script>
import HolaKubyhe from './components/HolaKubyhe.vue'
import FabKubyhe from './components/FabKubyhe.vue'
import OMVKubyhe from './components/OMVKubyhe.vue'
import ProductoK from './components/ProductoK.vue'
import contactoK from './components/contactoK.vue'


export default {
  name: 'App',
  components: {
    HolaKubyhe,
    FabKubyhe,
    OMVKubyhe,
    ProductoK,
    contactoK
  },
     data() {
    return {
    componenteActual: 'HolaKubyhe',
      mostrarModal: true
    }
  },
  methods: {
    ocultarModal() {
      this.mostrarModal = false
    },
    cambiarContenido(componente) {
    this.componenteActual = componente;
    },
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body{
  width: 100%;
  margin: 0;
  background: #EEAECA;
  background: radial-gradient(circle,rgba(238, 174, 202, 1) 0%, rgba(148, 187, 233, 1) 100%);
  /* background: linear-gradient(306deg,rgba(238, 174, 202, 1) 0%, rgba(148, 187, 233, 1) 100%); */
  background-attachment: fixed;  
}

.img1 {
  max-width: 80%;
}

/* Estilos para el modal */
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 100;
}

.modal-content {
  background: white;
  padding: 30px;
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 5px 15px rgba(0,0,0,0.3);
}
button {
  margin: 10px;
  padding: 10px 20px;
  cursor: pointer;
}
/* Estilos para el modal */
/*estilo de entrada*/
    .logotextomovil {
        display: flex;
        flex-direction: row;
        align-items: center;
        width: fit-content;
}
        .logoytext {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
        width: 100%;

    }
      #logo {
        display: flex;
        align-content:flex-start;
        justify-content: flex-start;
        width: 120px;
        height: auto;
        flex-wrap: wrap;
        align-items:flex-start ;
        flex-direction: row;
        padding: 10px;
    }   

   .logotext {
        display: flex;
        align-content: center;
        justify-content: flex-start;
        color:rgb(0, 0, 0);

    }
  button.logotextomovil  {
  cursor: pointer;
  border-radius: 5px;
  padding: 0 5px 0 5px;
  }

/* estilo para contenido*/
.container {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.button-group {

}

.button-group button {
  padding: 5px 10px;
  margin: 5px 3px;
  font-size: 16px;
  cursor: pointer;
  background-color:rgba(185, 178, 84, 0.459);
  color: rgb(51, 51, 51);
  border: none;
  border-radius: 5px;
}

.content-display {
  padding: 0 20px;
  border-radius: 8px;
  min-height: 200px; /* Evita que el contenedor se colapse */
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Transiciones para que el cambio entre componentes sea suave */
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}

.fologoytext a {
  color: black;
}
        .fologoytext {
        background-color: #00000079;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        border-radius: 10px;
        font-size: 15px;
        color:rgb(0, 0, 0);
    }
      .fologoytext:hover { 
      color: #ffffff;
      box-shadow: inset 0 0 20px rgb(255, 250, 178), 0 0 10px rgb(255, 235, 144);
      /*outline-color: rgb(49, 137, 172);
      outline-offset: 80px;
      text-shadow: 1px 1px 4px #fff;*/
      }
      .botonContenido:hover {
      color: #ffffff;
      box-shadow: inset 0 0 20px rgba(49, 138, 172, 0.5), 0 0 20px rgba(49, 138, 172, 0.4);
      outline-color: rgba(49, 138, 172, 0);
      outline-offset: 80px;
      text-shadow: 1px 1px 6px #fff;
      }

      footer {

      }

</style>
