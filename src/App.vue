<script setup>
// Aprovechamos la versatilidad de la Composition API para poder importar recursos sin tenerlos que 'pasar' al data(). 
import heroImage from './assets/one-piece.jpg';

// Iteración 2a: Opción 1: Crear un Json y cargarlo. Podemos iterarlo directamente en el v-for
import timeline from './assets/timeline.json';
import ImageComponent from './ImageComponent.vue';
import CronoList from './CronoList.vue';
</script>

<script>

// Iteración 2a. Opción 2: usar el data() para exponer una propiedad del estado con el timeline cargado desde timeline.json, igual que se hacía en Ironhack labs

</script>

<template>
  <main id="main">
    <h1 id="title">One Piece</h1>
    <h2>Sere el rey de los piratas</h2>
     <!-- TODO: Transformar en componente -->
      <image-component legend="Logo One Piece" :image="heroImage" />
     <!-- Fin componente -->
    <section>
      <!-- <h3  id="tribute-info">Cronología de las temporadas One Pice</h3> -->
        <!-- TODO: Transformar en componente -->
       <crono-list :items="timeline" />
      <!-- Fin componente -->

      </section>
       <image-component legend="To Be Continue"
      image="https://i.ytimg.com/vi/vvwzG6G18Ow/maxresdefault.jpg" />

      <a id="tribute-link" href="https://es.wikipedia.org/wiki/Anexo:Episodios_de_One_Piece" target="_blank">
       Fuente: Wikipedia, episodios de One Piece</a>
  </main>

</template>

<style>
@import './assets/base.css';

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

figure {
  border: thin #c0c0c0 solid;
  display: flex;
  flex-flow: column;
  padding: 5px;
  margin: auto;
}

img {
  max-width: 100%;
}

figcaption {
  background-color: #222;
  color: #fff;
  font-style: italic;
  font-weight: 700;
  padding: 3px;
  text-align: center;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (min-width: 1024px) {
  body {
    display: flex;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }
}
</style>
