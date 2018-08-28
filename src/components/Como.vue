<template>
    <div id="como">
        <div class="fale">
            <h1>Como trabalhamos</h1>
        </div>
        <div class="btn-1" v-if="counter > 0" v-on:click="counter -= 1">
            <i class="fas fa-arrow-left"></i>
        </div>
        <div class="como-wrap" v-bind:class="colors[counter]"></div>
        <div class="btn-2" v-if="counter < colors.length - 1" v-on:click="counter += 1">
            <i class="fas fa-arrow-right"></i>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Como',
  data: function () {
      return {
          counter: 0,
          colors: ["bg-1", "bg-1-2", "bg-2", "bg-2-2", "bg-3", "bg-3-2"]
      }
  }
}
</script>

<style scoped>
#como {
    width: 100%;
    min-height: 100vh;
    background-color: var(--cinza-5);
    display: grid;
    grid-template-columns: 15vw 1fr 15vw;
    grid-template-rows: 12vh 10vh 1fr 10vh;
    align-items: center;
    justify-items: center;
}
.fale {
  background-color: var(--cinza-4);
  display: flex;
  grid-column: span 3;
  justify-self: start;
  width: 100%;
  height: 100%;
  }
.fale h1 {
  margin: 0;
  margin-left: 10vw;
  text-transform: uppercase;
  color: var(--cinza-2);
  align-self: center;
  font-size: 5vh;
}
.bg-1 {
    background-image: url('../assets/como-pg-1-1.jpg');
}
.bg-1-2 {
    background-image: url('../assets/como-pg-1-2.jpg');
}
.bg-2 {
    background-image: url('../assets/como-pg-2-1.jpg');
}
.bg-2-2 {
    background-image: url('../assets/como-pg-2-2.jpg');
}
.bg-3 {
    background-image: url('../assets/como-pg-3-1.jpg');
}
.bg-3-2 {
    background-image: url('../assets/como-pg-3-2.jpg');
}

.btn-1, .btn-2 {
    width: 50px;
    height: 50px;
    background-color: var(--cinza-1);
    color: white;
    font-size: 30px;
    display: grid;
    align-items: center;
    justify-items: center;
    cursor: pointer;
}

.btn-1 {
    grid-row: 3;
    grid-column: 1;
}
.btn-2 {
    grid-row: 3;
    grid-column: 3;
}
.como-wrap {
    width: 67.7vw;
    height: 41.66vw;
    border: 1px solid var(--cinza-2);
    grid-column: 2;
    grid-row: 3;
    background-position: center;
    background-size: cover;
}
@media (max-width: 768px) {
    .btn-1, .btn-2 {
        width: 40px;
        height: 40px;
        font-size: 20px;
    }
    .como-wrap {
        width: 100%;
        height: 100%;
    }
}
</style>
