<template>
    <div id="quem">
        <div class="quem-img" v-on:click="counter < 1 ? counter += 1 : counter = 0" v-bind:class="img[counter]"></div>
        <div class="quem-txt">
            <h3>RACHEL CANTO FIGUEIREDO</h3>
            <small>Advogada associada</small>
            <p>Advogada e bacharel em Direito pela Universidade Presbiteriana Mackenzie, com experiência internacional na Faculdade de Direito da Universidade Nova de Lisboa.</p>
            <p>Atuante nas áreas cível e comercial. Experiência tanto no consultivo quanto no contencioso e  em meios alternativos à resolução de conflitos.</p>
            <p>Perfil diversificado pela passagem por  escritórios "Boutique"  e de médio porte,  nas seguintes áreas:</p>
            <p>de Família e Sucessões; Imobiliário; Responsabilidade Civil; Direito do Consumidor;  Insolvência e Reestruturação de Dívidas, incluindo a recuperação de créditos.</p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Rachel',
  data: function () {
      return {
          counter: 0,
          img: ["img1", "img1-2"]
      }
    }
}
</script>

<style scoped>
#quem {
    width: 100%;
    height: 100vh;
    display: grid;
    grid-template-columns: 36vw 1fr;
    box-sizing: border-box;
}
.quem-img {
    background-size: cover;
    min-height: 50vh;
    cursor: pointer;
}
.img1 {
    background-image: url('../assets/img3916.jpg');
    transition: all 0.3s ease;
}

.img1-2 {
    background: 
    linear-gradient(var(--vermelho), var(--vermelho)),
    url('../assets/img3916.jpg');
    background-blend-mode: color;
    background-size: cover;
    transition: all 0.8s ease;
}

.quem-txt {
    background-color:var(--camelo);
    color: var(--cinza-5);
    padding: 5vh 15vw 5vh 5vw;
}
h3 {
    margin-top: 10vh;
    color: var(--cinza-5);
    font-size: 3.5vh;
    margin-bottom: 1vh;
}
small {
    font-size: 2vh;
}
p {
    font-family: var(--esteban);
    font-size: 2.5vh;
}
p:first-of-type {
    margin-top: 5vh;
}

@media (max-width: 768px) {
    #quem {
        grid-template-columns: 1fr;
        grid-template-rows: 1fr 1fr;
    }
    .quem-img {
        background-position-y: -18vh;
    }
}
</style>
