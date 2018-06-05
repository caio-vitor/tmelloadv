<template>
  <div id="app">
    <Hero/>
    <Nav/>
    <div class="prlx img1"></div>
    <Quem/>
    <div class="prlx img2"></div>
    <Como/>
    <div class="prlx img3"></div>
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
}

.img1 {
  background-image: url('./assets/img0807.jpg');
}
.img2 {
  background-image: url('./assets/img3945.jpg');
}
.img3 {
  background-image: url('./assets/img3955.jpg');
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
