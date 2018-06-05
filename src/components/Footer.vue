<template>
  <footer>
      <p>Todos os direitos reservados &copy; TMello Advocacia, 2018.</p>
      <p><i class="fas fa-code"></i>&#32; desenvolvido por &#32;<i class="far fa-user"></i></p>  
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
footer {
    width: 100%;
    height: 5vh;
    background-color: var(--cinza-2);
    display: grid;
    grid-template-columns: 70vw 1fr;
    align-items: center;
    
}
p {
    margin: 0;
    margin-left: 2vw;
    font-size: 1.2vh;
    color: var(--cinza-4);
    align-self: center;
}
span {
    margin: 0;
    padding: 0;
    justify-self: center;
    display: flex;
}
img {
    margin-left: 10px;
}
</style>


