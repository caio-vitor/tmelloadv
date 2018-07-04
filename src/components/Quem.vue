<template>
    <div id="quem-somos">
        <div class="fale">
            <h1>Quem Somos</h1>
        </div>
        <div class="quem-wrap">
            <transition name="botão">
            <button v-if="show" @click="show = !show"><i class="fas fa-arrow-right"></i></button>
            <button v-else @click="show = !show"><i class="fas fa-arrow-left"></i></button>
            </transition>
            <transition name="quemsomos" mode="out-in">
                <Teresa v-if="show"></Teresa>
                <Rachel v-else></Rachel>
            </transition>
        </div>
    </div>
</template>

<script>
import Teresa from './Teresa.vue'
import Rachel from './Rachel.vue'

export default {
  name: 'Quem',
  data: function () {
      return {
          show: true
      }
  },
  components: {
      Teresa,
      Rachel
  }
}
</script>

<style scoped>
#quem-somos {
    min-height: 100vh;
}
.fale {
  background-color: var(--cinza-5);
  display: flex;
  height: 18vh;
}
.fale h1 {
  margin: 0;
  margin-left: 10vw;
  text-transform: uppercase;
  color: var(--cinza-2);
  align-self: center;
  font-size: 7vh;
}
.quem-wrap {
    position: relative;
}
button {
    position: absolute;
    top: 50%;
    right: 1.5vw;
    border: none;
    box-shadow: none;
    background-color: var(--vermelho);
    color: white;
    width: 40px;
    height: 40px;
    font-weight: 700;
    font-size: 2vh;
    text-align: center;
    cursor: pointer;
    outline: 0;
    z-index: 1;
}
@media (max-width: 768px) {
    button {
        top: 52vh;
        right: 2vh;
    }
}

</style>
