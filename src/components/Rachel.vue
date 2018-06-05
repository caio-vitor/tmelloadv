<template>
    <div id="quem">
        <div class="quem-img"></div>
        <div class="quem-txt">
            <h3>RACHEL CANTO FIGUEIREDO</h3>
            <small>Advogada associada</small>
            <p>Rachel é advogada e bacharel em Direito pela Universidade Presbiteriana Mackenzie, com experiência internacional na Faculdade de Direito da Universidade Nova de Lisboa.</p>
            <p>Atuante nas áreas cível e comercial, com experiência tanto no consultivo quanto no contencioso, bem como meios alternativos à  resolução de conflitos visando a  prevenção de litígios. Sua  experiência é diversificada em escritórios "Boutique" e médio porte, notadamente nas áreas de Família e Sucessões; Imobiliário; Responsabilidade Civil; Direito do Consumidor;  Insolvência e Reestruturação de Dívidas, incluindo a recuperação de créditos.</p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Rachel'
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
    background-image: url('../assets/img3916.jpg');
    background-size: cover;
    min-height: 50vh;
}
.quem-txt {
    background-color: white;
    color: var(--cinza-4);
    padding: 5vh 15vw 5vh 5vw;
}
h3 {
    margin-top: 10vh;
    color: var(--camelo);
    font-size: 3.5vh;
    margin-bottom: 1vh;
}
small {
    font-size: 1.5vh;
}
p {
    font-family: var(--esteban);
    font-size: 1.6vh;
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
