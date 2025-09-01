<template>
  <div class="productos-container">
    <FichaProducto 
      v-for="producto in productos"
      :key="producto.id"
      :producto="producto"
    />
  </div>
</template>

<script>
import FichaProducto from './FichaProducto.vue'; // Importa el nuevo componente

import blusa34v from './kubyhe/prenda/blusa34-v.jpg';
import blusapantalonc  from './kubyhe/prenda/blusa-pantalon-c.webp';
import blusafaldac from './kubyhe/prenda/blusa-falda-c.webp';
import blusa34c from './kubyhe/prenda/blusa3-4c.jpg';
import blusacb from './kubyhe/prenda/blusa-c-b.jpg';
import camisac from './kubyhe/prenda/camisa-c.jpg';
import camisacg from './kubyhe/prenda/camisa-c-g.jpg';
import camisalc from './kubyhe/prenda/camisalc.webp';
import camisamc from './kubyhe/prenda/camisamc.png';
import variedad from './kubyhe/prenda/variedad.webp';

variedad.png
/* import   from './kubyhe/prenda/.jpg';*/

export default {
  name: 'ProductoK',
  components: {
    FichaProducto
  },
  data() {
    return {
      productos: [
        {
        id: 1,
        imagen: blusa34v,
        titulo: 'Blusa para dama',
        descripcion: 'Blusa en lino a rayas, color verde olivo, manga 3/4',
        informacionCompleta: ''
      },
      {
        id: 2,
        imagen: camisalc,
        titulo: 'Camisa de manta para Caballero',
        descripcion: 'Camisa en manta, con cuello, estilo Huasteco, manga larga, color beige',
        informacionCompleta: ''
      },
      {
        id: 3,
        imagen: blusafaldac,
        titulo: 'Conjunto Blusa y Falda larga',
        descripcion: 'Confeccionado en material manta de color natural, blusa manga corta y falda bolillo en manta ensamblada ajustable',
        informacionCompleta: ''
      },
      {
        id: 4,
        imagen: blusa34c,
        titulo: 'Blusa de Lino para dama',
        descripcion: 'Blusa con manga 3/4, material Lino bordado, color beige',
        informacionCompleta: ''
      },
      {
        id: 5,
        imagen: blusacb,
        titulo: 'Blusa de Lino bordado para Dama',
        descripcion: 'Blusa en lino color beige, bordado color verde, manga corta',
        informacionCompleta: ''
      },
      {
        id: 6,
        imagen: camisac,
        titulo: 'Camisa de Lino para Caballero',
        descripcion: 'Camisa en lino, manga corta, cuello corto o sport, color beige, botones superiores a la vista, botones inferiores ocultos',
        informacionCompleta: ''
      },
      {
        id: 6,
        imagen: camisamc,
        titulo: 'Camisa de Manta y Lino para Caballero',
        descripcion: 'Camisa en combinación Manta y Lino, manga corta, cuello corto o sport',
        informacionCompleta: ''
      },      
      {
        id: 8,
        imagen: camisacg,
        titulo: 'Camisa de Lino para Caballero',
        descripcion: 'Camisa en lino, cuello corto o sport, estilo Huasteco, manga corta, color beige',
        informacionCompleta: ''
      },
      {
        id: 9,
        imagen: blusapantalonc,
        titulo: 'Conjunto Blusa y Pantalón para dama',
        descripcion: 'Conjunto de blusa y pantalón de manta, color natural',
        informacionCompleta: ''
      },            
      {
        id: 10,
        imagen: variedad,
        titulo: 'Variedad de Prendas',
        descripcion: 'Vestidos para niña, Blusas para Dama y Camisas para Caballero',
        informacionCompleta: ''
      }
      ]
    };
  }
};
</script>

<style scoped>
.productos-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

/* Media Query para pantallas de escritorio.
  Cuando la pantalla tiene un ancho mínimo de 768px (o más),
  se aplican estos estilos.
*/
@media (min-width: 768px) {
  .productos-container {
    flex-direction: row; /* Vuelven a ser filas */
    flex-wrap: wrap;     /* Permite que los productos pasen a la siguiente fila */
    justify-content: center;
    max-width: 1200px;   /* Reduce el ancho máximo del contenedor */
    margin: 0 auto;      /* Centra el contenedor en la pantalla */
    gap: 20px;           /* Añade espacio entre los productos */
  }
}
</style>