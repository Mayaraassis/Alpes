<template>
  <div id="app">
    <headerComponent></headerComponent>
    <formCotacao></formCotacao>
    <bannerComponent></bannerComponent>
    <h1>Escolha Seu BMW</h1>
    <div class="cars">
      <cardComponent :carro="require('@/assets/serie1.png')" title="BMW Série 1"></cardComponent>
      <cardComponent :carro="require('@/assets/m3.png')" title="BMW M3 Competition"></cardComponent>
      <cardComponent :carro="require('@/assets/m5.png')" title="BMW M5"></cardComponent>
      <cardComponent :carro="require('@/assets/x2.png')" title="BMW X2"></cardComponent>
      <cardComponent :carro="require('@/assets/serie-4.png')" title="BMW Série 4"></cardComponent>
      <cardComponent :carro="require('@/assets/serie-3.png')" title="BMW Série 3"></cardComponent>
      <cardComponent :carro="require('@/assets/z4.png')" title="BMW Z4"></cardComponent>
      <cardComponent :carro="require('@/assets/serie2.png')" title="BMW Série 2"></cardComponent>
    </div>
    <footerComponent></footerComponent>
  </div>
</template>

<script>
import headerComponent from './components/header.vue'
import formCotacao from './components/formCotacao.vue';
import bannerComponent from './components/banner.vue';
import cardComponent from './components/card.vue';
import footerComponent from './components/footer.vue';
export default {
  name: 'App',
  components: {
    headerComponent,
    formCotacao,
    bannerComponent,
    cardComponent,
    footerComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}

body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.icon {

  filter: invert(41%) sepia(19%) saturate(6%) hue-rotate(321deg) brightness(90%) contrast(84%);
}

.icon:hover {
  cursor: pointer;
  filter: invert(27%) sepia(97%) saturate(1378%) hue-rotate(198deg) brightness(100%) contrast(90%);
}

@media(min-width: 765px) {
  .cars {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 20px;
    justify-content: center;
    margin: 60px 200px;
  }
}</style>
