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
                informacion: 'Blusa en lino bordado, color beige, manga 3/4',
            },
            { 
                id: 2,
                imagen: blusacb ,
                informacion: 'Blusa en lino bordado, color verde, manga corta',
            },
            { 
                id: 3,
                imagen: camisac,
                informacion: 'Camisa en lino, botones superiores a la vista, botones inferiores ocultos',
            },
            { 
                id: 4,
                imagen: camisacg ,
                informacion: 'Camisa en lino, estilo Huasteco',
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