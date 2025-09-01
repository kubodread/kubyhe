<template>

  <div class="colProd">
    <TxtRopa />
    <div class="productos-container">
      <FichaProducto 
        v-for="producto in productos"
        :key="producto.id"
        :producto="producto"
      />
    </div>

  </div>

</template>

<script>
import FichaProducto from './FichaProducto.vue'; // Importa el nuevo componente
import TxtRopa from './TxtRopa.vue';


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
    FichaProducto,
    TxtRopa
  },
  data() {
    return {
      productos: [
        {
        id: 1,
        imagen: blusa34v,
        titulo: 'Blusa para dama',
        descripcion: 'Blusas de materiales en lino, manta y algodón, con diseños elegantes a rayas, color verde olivo, manga 3/4',
        informacionCompleta: 'Presentaciones en talla 32, 34, 36, 38 y 40'
      },
      {
        id: 2,
        imagen: camisalc,
        titulo: 'Camisa de manta para Caballero',
        descripcion: 'Camisa confeccionada en manta, lino o combinados, con cuello, estilo Huasteco, manga larga, color beige',
        informacionCompleta: 'Presentaciones en talla 32, 34, 36, 38, 40 y 42'
      },
      {
        id: 3,
        imagen: blusafaldac,
        titulo: 'Conjunto Blusa y Falda larga',
        descripcion: 'Confeccionado en materiales de algodón, manta y lino, de color natural, con manga corta. La falda bolillo en materiales de manta ensamblada o lino, ajustable',
        informacionCompleta: 'Presentaciones en talla 32, 34, 36, 38 y 40'
      },
      {
        id: 4,
        imagen: blusa34c,
        titulo: 'Blusa para dama',
        descripcion: 'Blusa con manga 3/4, material en manta o Lino bordado, color beige',
        informacionCompleta: 'Presentaciones en talla 32, 34, 36, 38 y 40'
      },
      {
        id: 5,
        imagen: blusacb,
        titulo: 'Blusa con bordado para Dama',
        descripcion: 'Blusa en lino o manta, color beige, bordados color verde, manga corta',
        informacionCompleta: 'Presentaciones en talla 32, 34, 36, 38 y 40'
      },
      {
        id: 6,
        imagen: camisac,
        titulo: 'Camisa para Caballero',
        descripcion: 'Camisa en manta, lino o combinado, manga corta, cuello corto o sport, color beige, luce botones superiores a la vista y botones inferiores ocultos',
        informacionCompleta: 'Presentaciones en talla 32, 34, 36, 38, 40 y 42'
      },
      {
        id: 6,
        imagen: camisamc,
        titulo: 'Camisa de manta y lino para Caballero',
        descripcion: 'Camisa en combinación de algodón, manta y lino, manga corta, cuello corto o sport',
        informacionCompleta: 'Presentaciones en talla 32, 34, 36, 38, 40 y 42'
      },      
      {
        id: 8,
        imagen: camisacg,
        titulo: 'Camisa de algodón, manta o Lino para Caballero',
        descripcion: 'Camisa cofeccionada en diferentes materiales de algodón, principalmente en manta y lino, cuello corto o sport, estilo moderno inspirado en estilos Huastecos, manga corta, color beige',
        informacionCompleta: 'Presentaciones en talla 32, 34, 36, 38, 40 y 42'
      },
      {
        id: 9,
        imagen: blusapantalonc,
        titulo: 'Conjunto Blusa y Pantalón para dama',
        descripcion: 'Conjunto de blusa y pantalón en algodón, color natural',
        informacionCompleta: 'Presentaciones en talla 32, 34, 36, 38 y 40'
      },            
      {
        id: 10,
        imagen: variedad,
        titulo: 'Variedad de Prendas',
        descripcion: 'Vestidos para niña, Blusas para Dama y Camisas para Caballero confeccionadas en distintos materiales',
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
.colProd {
  display: flex;
  flex-direction: column;
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