<template>
  <div class="ficha-producto">
    <img class="figt" :src="producto.imagen" :alt="producto.titulo">
    <div class="contenido-ficha">
      <h3>{{ producto.titulo }}</h3>
      <p>{{ producto.descripcion }}</p>
      <button @click="mostrarModal = true">Leer más</button>
    </div>

    <ModalB v-if="mostrarModal" @close="mostrarModal = false">
      <h2>{{ producto.titulo }}</h2>
          <img class="figt2" :src="producto.imagen" :alt="producto.titulo">
      <p>{{ producto.informacionCompleta }}</p>
      <button @click="mostrarModal = false">Cerrar</button>
    </ModalB>
  </div>
</template>

<script>
import ModalB from './ModalB.vue'; // Asume que ya tienes este componente

export default {
  name: 'FichaProducto',
  components: {
    ModalB
  },
  props: {
    producto: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      mostrarModal: false
    };
  }
};
</script>

<style scoped>
.ficha-producto {
  border: 1px solid #ccc;
  padding: 15px;
  margin: 10px;
  border-radius: 8px;
  text-align: center;
}
img {
  max-width: 100%;
  height: auto;
  border-radius: 4px;
}

        .figt {
        mask-image: linear-gradient( #1f2937 40%, transparent );
        justify-content: center;
        border-radius: 45px;
    }

  img.figt2 {
    min-height: 300px;
    max-height: 650px;
    border-radius: 45px;
  }

/* Media Query para escritorio */
@media (min-width: 768px) {
  .ficha-producto {
    /* Calcula el ancho para que quepan 2 o 3 fichas en una fila.
      calc() es muy útil para esto.
    */
    width: calc(33.33% - 20px); /* 33.33% - el espacio de gap */
    max-width: 350px; /* Evita que crezca demasiado */
  }

}
</style>