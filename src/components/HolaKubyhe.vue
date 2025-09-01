<template>
  <div class="hello">
    <h1>¡Bienvenidos!</h1>
   <br>
    <div class="cuadroTxt">
      <article> <br>
        Somos una empresa familiar 100% mexicana, con experiencia en la confección de prendas de vestir para dama, caballero y niña. 
        <br> <br> Con textiles de la más alta calidad, dedicados especialmente en manta, lino o combinada con otras texturas que puede ser algodón, en sus diferentes presentaciones.    
        <br> <br>
      </article>
    </div>

      <img class="img1" alt="Kubyhe Ver logo" src='../components/kubyhe/kyhv.webp'>

    <h3>
      Confección de ropa de manta, lino, tipo artesanal y casual para dama, caballero y niña.
    </h3>

    <TextoApp />

  </div>
</template>

<script>
import TextoApp from './TextoApp.vue';


export default {
  name: 'HolaKubyhe',
  props: {
    msg: String,
    txt1: String
  },
   components: {
    TextoApp
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}

.img1 {
  filter: sepia(2%);
  max-width:450px;
}
.img1:hover {
    filter: saturate(140%);
  }

.cuadroTxt {
  border: solid 1px;
  border-radius: 0.8em;
  background:rgba(201, 201, 201, 0.56);
  padding: 15px;
}



    .figt {
        display: flex;
        align-items: center;
        background-color: lightgray;
        border-radius: 15px;
        padding: 5px;
        mask-image: linear-gradient( #1f2937 90%, transparent );
    }
</style>
