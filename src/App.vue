<template>
   
     <div class="logoytext">
            <div class="logotextomovil">
                  <img id="logo" src="../src/assets/logok.webp" alt="Logo de KubyHe">   
            </div>
      <div class="logoytextHam">
    <button class="hamburger-menu" @click="toggleMenu">
      <span></span>
      <span></span>
      <span></span>
    </button>
    
    <div :class="['button-group', { 'is-open': isMenuOpen }]">
      <ul class="button-group-list">
        <li>
            <button class="botonContenido" @click="cambiarContenido('HolaKubyhe')" > &#10024; Inicio &#10024;</button>
        </li>
        <li>
            <button class="botonContenido" @click="cambiarContenido('FabKubyhe')"  >  Elaboración ✂️ </button>
        </li>
        <li>
            <button class="botonContenido" @click="cambiarContenido('OMVKubyhe')"  >Nuestra Esencia &#11088;</button>
        </li>
        <li>
            <button class="botonContenido" @click="cambiarContenido('ProductoK')"  >Productos &#128090;</button>
        </li>
        <li>
        <button class="botonContenido" @click="cambiarContenido('contactoK')"  >Contacto 	&#128222;</button>
        </li>

      </ul>
    </div>
  </div>
</div> 
<br>

 <Loader v-if="isLoading" />

 <div class="content-display-padding">
  <div v-show="!isLoading" class="content-display">
        <transition name="fade" mode="out-in">
          <component :is="componenteActual"></component>
        </transition>
      </div>
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
import { ref, watch } from 'vue';
import Loader from './components/Loader.vue';


export default {
  name: 'App',
  components: {
    HolaKubyhe,
    FabKubyhe,
    OMVKubyhe,
    ProductoK,
    contactoK,
    Loader
  },
      setup() {
    // Variables reactivas para el estado
    const isLoading = ref(false);
    const componenteActual = ref(HolaKubyhe);




    const isMenuOpen = ref(false);
    const toggleMenu = () => {
      isMenuOpen.value =!isMenuOpen.value;
    };

 


    // Método para cambiar el componente y manejar el loader
    const cambiarContenido = (componente) => {
      // Muestra el loader inmediatamente
      isLoading.value = true;
      // Asigna el nuevo componente
      componenteActual.value = componente;
      
      // Simula el tiempo de carga
      setTimeout(() => {
        // Oculta el loader cuando la carga "termina"
        isLoading.value = false;
      }, 400);
      isMenuOpen.value = false;

    };

    // Puedes usar watch aquí para observar componenteActual
    // si la lógica de carga fuera más compleja
    /*
    watch(componenteActual, (nuevoComponente) => {
      if (nuevoComponente) {
        isLoading.value = true;
        setTimeout(() => {
          isLoading.value = false;
        }, 100);
      }
    });
    */

    // Devuelve el estado y los métodos para que la plantilla pueda usarlos
    return {
      isLoading,
      componenteActual,
      cambiarContenido,
      isMenuOpen,
      toggleMenu,
    };
  },
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
        position: fixed;
        top: 0;
        z-index: 10;
        background-color: rgb(163 185 228 / 73%);

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
        padding: 5px 10px;
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
  background-color:rgba(163, 185, 228, 0.897);
  color: rgb(51, 51, 51);
  border: none;
  border-radius: 5px;
}

.content-display {
  padding: 40px 20px 0 20px;
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

        div.fologoytext {
        background-color: #00000079;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-size: 15px;
        color:rgb(0, 0, 0);
        width: fit-content;
        padding: 0 0;
        position: fixed;
        bottom: 0;
    }
      .fologoytext:hover { 
      color: #ffffff;
      box-shadow: inset 0 0 20px rgb(255, 250, 178), 0 0 10px rgb(255, 235, 144);
      /*outline-color: rgb(49, 137, 172);
      outline-offset: 80px;
      text-shadow: 1px 1px 4px #fff;*/
      }

      a {
        color: blue;
      }

      p.fologotext , a{
        color: black;
        font-weight: 600;
        width: fit-content;
        padding:  5px;
        margin: 0;
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


      /* Estilos para pantallas grandes (desktop) */
.hamburger-menu {
  display: none; /* Oculta el botón de hamburguesa en desktop */
}

.button-group-list {
  display: flex; /* Muestra los botones en fila */
  list-style: none;
  padding: 0;
  margin: 0;
}

.button-group-list li {
  margin: 0 10px;
}


/* Estilos para pantallas pequeñas (móviles) */
@media (max-width: 768px) {
  .hamburger-menu {
    display: block; /* Muestra el botón de hamburguesa */
    background: none;
    border: none;
    cursor: pointer;
    z-index: 100;
  }
  
  .hamburger-menu span {
    display: block;
    width: 25px;
    height: 3px;
    background-color: #333;
    margin: 5px 0;
  }
  
  .button-group {
    display: none; /* Oculta el menú por defecto */
    flex-direction: column;
    position: absolute;
    top: 60px; /* Ajusta esto a la altura de tu barra de navegación */
    left: 0;
    width: 100%;
    background-color: #fff;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    z-index: 99;
  }
  
  .button-group.is-open {
    display: flex; /* Muestra el menú cuando tiene la clase 'is-open' */
      background-color:rgb(163 185 228 / 73%);
      width: fit-content;
    border-radius: 5px;
  }
  
  .button-group-list {
    flex-direction: column;
    width: fit-content;
  }
  
  .button-group-list li {
    width: fit-content%;
    text-align: center;
    padding: 10px;
  }
  
      #logo {
        display: flex;
        align-content:flex-start;
        justify-content: flex-start;
        width: 100px;
        height: auto;
        flex-wrap: wrap;
        align-items:flex-start ;
        flex-direction: row;
        padding: 3px 10px;
    }  
  .button-group button {
  padding: 0 5px;
  margin: 0;
  font-size: 16px;
  cursor: pointer;
  background-color:rgba(163, 185, 228, 0.897);
  color: rgb(51, 51, 51);
  border: none;
  border-radius: 5px;
}

button {
  margin: 0;
  padding: 0;
  cursor: pointer;
}
.logoytextHam {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
.content-display-padding {
  padding-top: 20px;
}
}

</style>
