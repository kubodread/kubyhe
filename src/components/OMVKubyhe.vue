<template>
  <div class="hello">
    <h1>Nuestra Esencia</h1>
   <br>
    <div class="">
            <h2> Objetivo: </h2>
            <article class="figt">
              
              Lograr el desarrollo humano, económico, organizacional, elevando la calidad, la productividad y ubicación en un marcado mas competitivo, lo cual permitirá la consolidación de la empresa y de quienes participamos en el proceso productivo. 
            </article>
        
              <h2> Misión: </h2>
            <article class="figt">
            
              Empresa familiar, que se esmera por brindar el mejor servicio a su clientela, confeccionando ropa de manta, lino, tipo artesanal y casual, en línea y variedad de colores para dama, caballero y niña. <br> Proponiéndose crecer y desarrollarse como empresa, con responsabilidad y honestidad, entre y para quienes trabajamos en ella, reflejando armonía organizacional, asertividad y atención  al publico.
            </article>
  
              <h2> Visión: </h2>
            <article class="figt">
            
              Buscamos el crecimiento y desarrollo empresarial, económico, individual y grupalmente, logrando la excelencia. <br> En el diseño y el buen vestir permitiéndonos posicionarnos en el mercado nacional e internacional. 
            </article>

            
        <br>
        <div class="cuadroTxt">
            <h2>Nuestro Impacto Sostenible</h2>
            <article class="figt">
              El impacto social es favorable por la accesibilidad economica de nuestras prendas.
            </article>
            <article class="figt">
              El beneficio economico ha sido principalmente para los integrantes del grupo de trabajo, el cliente se beneficia al comprar directo AL PRODUCTOR.
            </article>
            <article class="figt">
              El medio ambiente no se deteriora, pues el proyecto no contamina.
            </article>
            <article class="figt">
              Se trata de inculcar en las nuevas generaciones a preservar las tradiciones y el gusto por la ropa con material natural y artesanal.
            </article>
        </div>
    </div>

      <img class="img1" alt="Vue logo" src='../components/kubyhe/kyhv.webp'>



  </div>
</template>

<script>



export default {
  name: 'OMVKubyhe',

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
}
.img1:hover {
    filter: saturate(140%);
  }

.cuadroTxt {
  border: solid 1px;
  border-radius: 0.8em;
  background:rgba(201, 201, 201, 0.32);
  padding: 15px;
}



    .figt {
        display: flex;
        align-items: center;
        background-color: lightgray;
        border-radius: 15px;
        padding: 15px;
        mask-image: linear-gradient( #1f2937 90%, transparent );
    }

.mi-lista-elaboracion {
  display: flex;
  padding: 0;
  flex-direction: column;
}
</style>
