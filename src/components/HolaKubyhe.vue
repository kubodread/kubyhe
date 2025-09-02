<template>
  <div class="hello">
  
    <img class="img1" alt="Kubyhe Ver logo" src='../components/kubyhe/kyhv.webp'>
      <TxtRopa />  <br>
    <div class="cuadroTxth">
      <article> <br>
        <h4>
          Somos una empresa familiar 100% mexicana, con experiencia en la confección de prendas de vestir para dama, caballero y niña. 
        </h4>
     Con textiles de la más alta calidad, elaborados especialmente en manta, lino o combinada con otras texturas que puede ser algodón, en sus diferentes presentaciones.    
        <br> <br>
      </article>
    </div>
    <br>

    <TextoApp />




  </div>
</template>

<script>
import TextoApp from './TextoApp.vue';
import TxtRopa from './TxtRopa.vue';


export default {
  name: 'HolaKubyhe',
  props: {
    msg: String,
    txt1: String
  },
   components: {
    TextoApp,
    TxtRopa
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
  width: 70%;
  margin: -40px 0;

}
.img1:hover {
    filter: saturate(140%);
  }

.cuadroTxth {
  border-radius: 0.8em;
  background:rgba(201, 201, 201, 0.322);
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
