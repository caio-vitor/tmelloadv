<template>
  <div id="app">
    <Hero/>
    <Nav/>
    <div class="prlx" v-on:click="counter1 < 2 ? counter1 += 1 : counter1 = 0" v-bind:class="img1[counter1]">
      <p>clique na imagem para ver mais opções</p>
    </div>
    <Quem/>
    <div class="prlx" v-on:click="counter2 < 1 ? counter2 += 1 : counter2 = 0" v-bind:class="img2[counter2]"><p>clique na imagem para ver mais opções</p></div>
    <Como/>
    <div class="prlx" v-on:click="counter3 < 1 ? counter3 += 1 : counter3 = 0" v-bind:class="img3[counter3]"><p>clique na imagem para ver mais opções</p></div>
    <Contato/>
    <Footer/>
  </div>
</template>

<script>
import Hero from './components/Hero.vue'
import Nav from './components/Nav.vue'
import Quem from './components/Quem.vue'
import Como from './components/Como.vue'
import Contato from './components/Contato.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  components: {
    Hero,
    Nav,
    Quem,
    Como,
    Contato,
    Footer
  },
  data: function () {
      return {
          counter1: 0,
          counter2: 0,
          counter3: 0,
          img1: ["img1", "img1-2", "img1-3"],
          img2: ["img2", "img2-2"],
          img3: ["img3", "img3-2"]
      }
  }
}
</script>

<style>
#app {
  font-family: var(--mont);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0;
}
.prlx {
  height: 80vh;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  cursor: pointer;
  display: grid;
  grid-template-rows: 8fr 1fr;
  align-items: end;
}

.prlx p {
  margin: 0;
  color: white;
  text-align: center;
  font-family: var(--mont);
  font-weight: 700;
  text-shadow: 3px 3px black;
}

.img1 {
  background-image: url('./assets/img0807.jpg');
  transition: all 0.8s ease;
}
.img1-2 {
  background: 
  linear-gradient(rgba(0, 0, 0, 1), rgba(0, 0, 0, 1)),
  url('./assets/img0807.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-blend-mode: color;
  transition: all 0.8s ease;
}
.img1-3 {
  background: 
  linear-gradient(var(--camelo), var(--camelo)),
  url('./assets/img0807.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-blend-mode: color;
  transition: all 0.8s ease;
}

.img2 {
  background-image: url('./assets/img3859.jpg');
  transition: all 0.8s ease;
}
.img2-2 {
  background: 
  linear-gradient(rgba(0, 0, 0, 1), rgba(0, 0, 0, 1)),
  url('./assets/img3859.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-blend-mode: color;
  transition: all 0.8s ease;
}
.img3 {
  background-image: url('./assets/img3955.jpg');
  transition: all 0.8s ease;
}
.img3-2 {
  background: 
  linear-gradient(var(--vermelho), var(--vermelho)),
  url('./assets/img3955.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-blend-mode: color;
  transition: all 0.8s ease;
}
@media (max-width: 768px) {
  .prlx {
    height: 50vh;
    background-attachment: scroll;

  }
  .img2 {
    background-position-x: -15vw;
  }
}
</style>
