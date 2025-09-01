<template>
  <div class="hello">
    <h1>Proceso de Elaboración</h1>
    <h3>
      Confección de ropa de manta, lino, tipo artesanal y casual para dama, caballero y niña.
    </h3>
    <br>
    <div class="cuadroTxt">
      <h2>
      Proceso Artesanal: Creando Nuestras Prendas

    </h2>
    <article>
      Cada pieza que ves, es el resultado de un viaje meticuloso, lleno de dedicación y cuidado. No solo creamos ropa; tejemos historias con cada hilo. Nuestro proceso artesanal se inspira en la tradición, pero se adapta a la vida moderna, garantizando una prenda única y de la más alta calidad.
    </article>

    <ol class="mi-lista-elaboracion">
        <li class="figt">
            <article>
                <h3>Selección de Materia Prima: El Corazón de la Creación</h3>
                <p>Todo comienza con una búsqueda de la perfección. Seleccionamos personalmente las mejores mantas, un material que no solo es suave y cómodo, sino que también respira con la calidez de la tierra. Elegimos solo lo más puro, asegurando que cada prenda se sienta tan bien como se ve.</p>
            </article>
        </li>
        <li  class="figt">
            <article>
                <h3>Diseño: Un Encuentro entre Tradición y Vanguardia</h3>
                <p>Nuestros diseños son una celebración de lo atemporal. Con cada modelo, buscamos armonía, fluidez y una estética que hable de elegancia sin esfuerzo. Cada línea y cada corte están pensados para honrar la belleza natural de la manta, creando piezas que son tan únicas como la persona que las usa.</p>
            </article>
        </li>
        <li class="figt">
            <article>
                <h3>Corte Artesanal: Precisión y Cuidado en Cada Trazo</h3>
                <p>A diferencia de la producción en masa, cada pieza de tela se corta a mano con tijera. Este paso es un arte en sí mismo, donde la precisión y la experiencia de una artesana son cruciales. Un corte manual garantiza que cada línea sea exacta, preparando la prenda para un ajuste impecable.</p>
            </article>
        </li>
        <li class="figt">
            <article>
                <h3>Confección: Tejiendo Historias con Hilo y Aguja</h3>
                <p>Con nuestras manos, cada pieza cortada se une. Este es el momento en que la tela cobra vida. El ensamblado es un acto de cuidado, donde cada puntada es un testimonio de la calidad que valoramos. Nos enfocamos en la resistencia y el detalle, asegurando una costura que durará toda la vida.</p>
            </article>
        </li>
        <li class="figt">
            <article>
                <h3>Toques Finales: El Arte en los Pequeños Detalles</h3>
                <p>La belleza de una prenda a menudo reside en sus detalles. Cada ojal es una pequeña obra de arte, y cada botón se cose a mano, con una firmeza que solo un trabajo bien hecho puede garantizar. Finalmente, la prenda se plancha con cuidado, revelando su forma y textura final antes de ser empacada. Es el toque de gracia que prepara tu nueva prenda para su gran debut.</p>
            </article>
        </li>
    </ol>

    </div>

          <img class="img1" alt="Kubyhe logo" src='../components/kubyhe/kyhv.webp'>
    <div class="cuadroTxt">
      <article> <br>
        Somos una empresa familiar 100% mexicana, con experiencia en la confección de prendas de vestir para dama, caballero y niña. 
        <br> <br> Con textiles de la más alta calidad, dedicados especialmente en manta, lino o combinada con otras texturas que puede ser algodón, en sus diferentes presentaciones.    
        <br> <br>
      </article>
    </div>

  </div>
</template>

<script>


export default {
  name: 'FabKubyhe',
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
  width: 80%;
  filter: sepia(2%);
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

.mi-lista-elaboracion {
  display: flex;
  padding: 0;
  flex-direction: column;
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
