<template>
  <nav>
      <a href="#hero" class="logo"></a>
      <ul>
            <Button link="#quem-somos" tipo="Quem Somos" />
            <Button link="#como" tipo="Como Trabalhamos" />
            <Button link="#contato" tipo="Fale Conosco" />
      </ul>
  </nav>
</template>

<script>
import Button from './Button.vue'

export default {
  name: 'Nav',
  components: {
      Button
  }
}
</script>

<style scoped>
nav {
    width: 100%;
    height: 8vh;
    background-color: var(--cinza-1);
    display: grid;
    grid-template-columns: 34vw 1fr;
    position: sticky;
    top: 0;
    z-index: 2;
}
.logo {
    width: 10vw;
    background-image: url('../assets/logo-badge.svg');
    background-size: 3.2vw;
    background-repeat: no-repeat;
    background-position: center;
    justify-self: start;
}
ul {
    list-style: none;
    display: flex;
    align-items: center;
    justify-self: start;
    text-transform: uppercase;
}
li {
    margin-right: 3.6vw;
}
a{
    text-decoration: none;
    color: white;
}
@media (max-width: 768px) {
    .logo {
        margin-left: 5vw;
        background-size: 8vw;
        justify-self: start;
    }
    ul {
        display: none;
    }
}
@media (max-width: 640px) {
    .logo {
        background-size: 10vw;
    }
}
</style>


