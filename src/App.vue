<template>
  <main id="main" class="container">
    <!-- Presentacion e imagen patateras -->
    <article class="info--article">
      <h1 id="title">Solanum tuberosum</h1>
      <h2>Llamada vulgarmente como patata</h2>
        <blockquote class="blockquote">
          <p class="mb-0">Es un error creer que cualquier problema importante puede solucionarse
          con ayuda de unas patatas.</p>
          <footer class="blockquote-footer"><cite title="Douglas Adams">Douglas Adams</cite></footer>
        </blockquote>
      <!-- Componente donde mostramos una imagen y un caption -->
      <imgComponent name="Solanum tuberosum" imgUrl="https://s1.eestatic.com/2020/10/09/ciencia/nutricion/patatas-adelgazar-dieta_526958892_162156492_1024x576.jpg" caption="Sociedad compleja de tuberculos amigables."/>
    </article>

    <article class="list--article">
      <h1>Variedad de patatas:</h1>
      <!-- Lista de variedades de patata -->
      <cronoList :patataList="patataList"/>

      <!-- Componente donde mostramos una imagen y un caption -->
      <imgComponent name="Variedad de ptatas" imgUrl="https://phantom-elmundo.unidadeditorial.es/96cc6e0ffba61784307636367ff2ca25/resize/414/f/jpg/assets/multimedia/imagenes/2019/11/13/15736646476653.jpg" caption="Una patata al día da alegría"/>
    </article>

    <!-- Footer --> 
    <footer>
      <p>Si el conocimiento es tu pasion te dejo mas datos sobre estos amigables tuberculos <a id="tribute-link" href="https://es.wikipedia.org/wiki/Solanum_tuberosum" target="_blank"> Aqui</a></p>
    </footer>
    

  </main>
</template>

<script>
import imgComponent from "./components/imgComponent.vue";
import cronoList from "./components/CronoList.vue"
import patata from "./assets/patata.json"
export default {
  name: "App",
  data(){
    return{
      patataList: patata
    }
  },
  components: {
    imgComponent,
    cronoList
  },
};
</script>

<style>
:root{
  --color1: #F2CF63;
  --color2: #D9A74A;
  --color3: #A65712;
  --color4: #401201;  
}

body{
  background: linear-gradient(-45deg, var(--color1), var(--color2), var(--color3), var(--color4));
  background-size: 400% 400%;
  animation: gradient 15s ease infinite;
  height: 100vh;
}

article{
  background: var(--color1);
  padding: 1em;
  box-sizing: border-box;
}

/* Añadmimos un poco de interlineado */
.blockquote {
    line-height: 2em;
}

/* Animaciones */
@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
</style>