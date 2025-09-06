<template>
  <div class="esencia">
    <h1 class="omvt">Nuestra Esencia</h1>
   <br>
     <div class="videoYT">
    <iframe
      :src="videoUrl"
      title="¡TRIUNFANDO CON ICATVER - FAMILIA KUBOTA HERNÁNDEZ! "
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    ></iframe>
  </div>
    <div class="omvd">
      <div class="omvd">
            <img class="omv" alt="Kubyhe objetivos logo" src='../components/kubyhe/objetivos.svg'>
            <h2 class="omvt"> Objetivo: </h2>
            <article class="figt">
              
              Lograr el desarrollo humano, económico, organizacional, elevando la calidad, la productividad y ubicación en un mercado más competitivo, lo cual permitirá la consolidación de la empresa y de quienes participamos en el proceso productivo. 
            </article>
                    <img class="omv" alt="Kubyhe mision logo" src='../components/kubyhe/mision.svg'>
              <h2 class="omvt"> Misión: </h2>
            <article class="figt">
            
              Empresa familiar, que se esmera por brindar el mejor servicio a su clientela, confeccionando ropa de manta, lino, tipo artesanal y casual, en línea y variedad de colores para dama, caballero y niña. <br> Proponiéndose crecer y desarrollarse como empresa, con responsabilidad y honestidad, entre y para quienes trabajamos en ella, reflejando armonía organizacional, asertividad y atención  al publico.
            </article>
              <img class="omv" alt="Kubyhe vision logo" src='../components/kubyhe/vision.svg'>
              <h2 class="omvt"> Visión: </h2>
            <article class="figt">
            
              Buscamos el crecimiento y desarrollo empresarial, económico, individual y grupalmente, logrando la excelencia. <br> En el diseño y el buen vestir permitiéndonos posicionarnos en el mercado nacional e internacional. 
            </article>         
      </div>
        <br>
        <div class="cuadroTxt ">
            <h2>Nuestro Impacto Sostenible</h2>
            <article class="figt">
              El impacto social es favorable por la accesibilidad economica de nuestras prendas.
            </article>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/economico.svg'>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/vestir.svg'>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/economicoparte.svg'>

            <article class="figt">
              El beneficio económico ha sido principalmente para los integrantes del grupo de trabajo, el cliente se beneficia al comprar directo AL PRODUCTOR.
            </article>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/personal.svg'>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/amorv.svg'>

            <article class="figt">
              El medio ambiente no se deteriora, pues el proyecto no contamina.
            </article>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/arbolv.svg'>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/ciudadv.svg'>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/mundov.svg'>

            <article class="figt">
              Se trata de inculcar en las nuevas generaciones a preservar las tradiciones y el gusto por la ropa con material natural y artesanal.
            </article>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/persona.svg'>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/nuevo.svg'>
            <img class="omv" alt="Kubyhe verde logo" src='../components/kubyhe/corazon.svg'>

        </div>
    </div>

      <img class="img1" alt="Kubyhe logo" src='../components/kubyhe/kyhv.webp'>



  </div>
</template>

<script>



export default {
  name: 'OMVKubyhe',
data() {
    return {
      // Reemplaza con la ID del video de YouTube que deseas mostrar
      videoId: 'Ir7JCh_v5KY', // Ejemplo: la ID de un video de Rick Astley
      videoUrl: ''
    };
  },
  mounted() {
    // Construye la URL de YouTube de forma dinámica
    this.videoUrl = `https://www.youtube.com/embed/${this.videoId}`;
  }
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
  width: 60%;
  margin: -30px;
}
.img1:hover {
    filter: saturate(140%);
  }

.cuadroTxt {
  border-radius: 0.8em;
  background:rgba(201, 201, 201, 0.32);
  padding: 15px;
}



    .figt {
        display: flex;
        align-items: center;
        background-color: rgba(211, 211, 211, 0.438);
        color: black;
        border-radius: 15px;
        padding: 15px;
        justify-content: center;
        /* mask-image: linear-gradient( #1f2937 70%, transparent ); */
    }

.mi-lista-elaboracion {
  display: flex;
  padding: 0;
  flex-direction: column;
}

.omv {
  width: 100px;
  height: auto;
}

.omvt {
  margin: -10px;
}

.omvd {
  margin: 5px;
}
  .esencia {
    padding-top: 20px;
  }

 
  .videoYT iframe {
      width: 100%;
      height: auto;
  }
  


@media (min-width: 768px) {
.omv {
  width: 100px;
  height: auto;
}

.omvt {
  margin: -10px;
}

.omvd {
  margin: 40px;
}
      .esencia {
    padding-top: 40px;
  }

  .videoYT iframe {
      width:660px;
      height:415px;
  }

}
</style>
