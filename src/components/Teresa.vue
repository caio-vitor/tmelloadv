<template>
    <div id="quem">
        <div class="quem-img" v-on:click="counter < 1 ? counter += 1 : counter = 0" v-bind:class="img[counter]"></div>
        <div class="quem-txt">
            <h3>TERESA CRISTINA MELLO DE ALMEIDA PRADO</h3>
            <p>Inicio da experiência em estágios em 1985, formando-se em 1989 pela Faculdade de Direito do Largo São Francisco.</p> 
            <p>Experiência muito diversificada junto a empresas, escritórios de advocacia empresarial, empresa de auditoria fiscal e como sócia de escritórios desde 1991.</p>
            <p>15 anos na advocacia empresarial e há 10 anos na advocacia cível e comercial com foco em questões patrimoniais, familiares e contratuais.</p>
            <p>Trabalho pautado pela exigência de qualidade e observação aos detalhes e aprofundamento da análise do caso. Acredita na necessidade de pacificar as relações, mantendo-se estudiosa da psicologia aplicada ao direito.</p>
            <p class="cv">Para CV completo, <a href="">clique aqui</a>.</p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Teresa',
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
    min-height: 100vh;
    display: grid;
    grid-template-columns: 36vw 1fr;
    box-sizing: border-box;
}
.quem-img {
    background-size: cover;
    background-position: right;
    min-height: 50vh;
    cursor: pointer;
}
.img1 {
    background-image: url('../assets/teresa.jpg');
    transition: all 0.3s ease;
}

.img1-2 {
    background: 
    linear-gradient(var(--camelo), var(--camelo)),
    url('../assets/teresa.jpg');
    background-blend-mode: color;
    background-size: cover;
    transition: all 0.8s ease;
}
.quem-txt {
    background-color: var(--cinza-2);
    color: var(--cinza-5);
    padding: 5vh 10vw 5vh 5vw;
}
h3 {
    margin-top: 10vh;
    margin-bottom: 1vh;
    font-size: 3.5vh;
    color: var(--camelo);
}
small {
    font-size: 1.5vh;
}
p {
    font-family: var(--esteban);
}
p:first-of-type {
    margin-top: 5vh;
}
b {
    color: white;
}

.cv {
    margin-top: 5vh;
    font-family: var(--mont);
    font-weight: 600;
    color: var(--camelo);
}

a {
    text-decoration: none;
}

a:visited {
    color: var(--vermelho);
}

@media (max-width: 768px) {
    #quem {
        grid-template-columns: 1fr;
        grid-template-rows: 1fr 1fr;
        max-height: 280vh;
    }
    .quem-img {
        background-position-y: -15vh;
    }
}
</style>
