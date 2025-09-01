<template>
    <div :class="claseContenedor">
        <ImgText 
            v-for="texto in textos"
            :key="texto.id"
            :texto="texto"
        />
    </div>
</template>


<script>
import ImgText from './ImgText.vue';

import blusa34c from './kubyhe/prenda/blusa3-4c.jpg';
import blusacb from './kubyhe/prenda/blusa-c-b.jpg';
import camisac from './kubyhe/prenda/camisa-c.jpg';
import camisacg from './kubyhe/prenda/camisa-c-g.jpg';


export default {
    name: 'TextoApp',
    components:{
        ImgText
    },
    data() {
        return {
                claseContenedor: 'claseContenedor',

            textos: [
            { 
                id: 1,
                imagen: blusa34c,
                informacion: '🌿 👚 ¡Viste con Comodidad y Elegancia Natural! 👚 🌿 ¿Buscas una prenda que te haga sentir cómoda, 🌸 elegante y conectada con la naturaleza? 🌿 🌞 ',
            },
            { 
                id: 2,
                imagen: blusacb ,
                informacion: '☀️ 👗 ¡Siente la Libertad y el Estilo con Nuestras Prendas de algodón, manta y/o lino! 👗 ☀️ ',
            },
            { 
                id: 3,
                imagen: camisac,
                informacion: '👚 👔 👕 Imagina una prenda que te brinde frescura ❄️ en los días cálidos ☀️ y un toque de sofisticación ✨ en cualquier momento 👕 👔 👚  ',
            },
            { 
                id: 4,
                imagen: camisacg ,
                informacion: '✨ ❄️ Descubre la frescura y el estilo único de nuestras blusas y camisas en manta, lino y algodón.❄️ ✨  ¡Encuentra tu prenda ideal y luce radiante! 🌞',
            },
            ],   
        }
    }
};

</script>


<style scoped>
.claseContenedor {
        display: flex;
        flex-direction: column;
        border: 3px;
        border-color: #3882f6;
        padding-top: 5px;
        justify-content: space-between;
        gap: 3px;
        align-items: start;
        flex-wrap: wrap;
        align-content: center;
    }


/* Media Query para pantallas de escritorio.
  Cuando la pantalla tiene un ancho mínimo de 768px (o más),
  se aplican estos estilos.
*/
@media (min-width: 768px) {
  .claseContenedor {
    flex-direction: row; /* Vuelven a ser filas */
    flex-wrap: wrap;     /* Permite que los productos pasen a la siguiente fila */
    justify-content: center;
    max-width: 1200px;   /* Reduce el ancho máximo del contenedor */
    margin: 0 auto;      /* Centra el contenedor en la pantalla */
    gap: 10px;           /* Añade espacio entre los productos */
  }
  }
</style>