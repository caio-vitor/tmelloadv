<template>
    <div id="quem">
        <div class="quem-img" v-on:click="counter < 1 ? counter += 1 : counter = 0" v-bind:class="img[counter]"></div>
        <div class="quem-txt">
            <h3>TERESA CRISTINA MELLO DE ALMEIDA PRADO</h3>
            <small>OAB/SP 107.110</small>
            <h5>30 anos de atuação</h5>
            <ul>
                <li>Formada em <b>Direito pela Faculdade de Direito do Largo São Francisco</b> (Universidade de São Paulo) em 1989 e com especialização  pelo  <b>CEEU (Centro de Estudos de Extensão Universitária) na área IR e Processo de Execução</b>;</li>
                <li><b>Pós graduação na GV LAW</b> em "Estratégias Societárias, Sucessórias e Tributação", 2009;</li>
                <li>FGV/2011: Direitos Humanos, com foco no Direito das Mulheres e Discriminação Racial;</li>
                <li>Membro de grupo de estudos regulares de psicologia, presidido  por psicóloga da Sociedade Brasileira de Psicologia Analítica, de 2012 a 2017;</li>
                <li>MEDIAÇÃO e técnicas, cursado no IASP, em 2012.</li>
            </ul>
            <h5>Cursos no exterior</h5>
            <p><b>Harvard Law School</b>, “Investimentos Estrangeiros em Países em Desenvolvimento”e Direito Tributário – 1988;  <b>Queen Mary & Westfield College, Universidade de Londres</b>: “Direito Tributário Internacional” e Direito do Comércio Internacional”, 1996; <b>Kings’s College, Universidade de Londres, “EC Law”</b> – Legislação da Comunidade Européia, Londres, 1996.</p>
            <p>Autora de diversos artigos e correspondente brasileira do periódico mensal britânico “World Tax Report” do Financial Times, de 1996 a 1998, e do periódico americano “Tax Notes International – TNI”, de 1991 a 1997.</p>
            <h5>Experiência profissional</h5>
            <ul>
                <li>Fundadora do <b>MELLO & KOUZNETZ com Adriana Kouznetz de Souza e Silva Fernandes há 5 anos em 2011 e desde 2017 atuando por TERESA MELLO Sociedade de Advogados</b>.</li>
                <li>2008 a 2010, como autônoma e consultora contratual e societária vinculada ao escritório <b>ADVOCACIA LUNARDELLI.</b></li>
                <li>Em 1991 fundou o escritório de advocacia empresarial, <b>ALMEIDA, MELLO E BRAGA</b>, onde atuou  por 10 (dez) anos, e foi responsável pela área de Direito Comercial, Societário e de Contratos, bem como Investimento estrangeiro/ Banco Central.</li>
                <li>Estágio no escritório PAISNER & CO., Londres, na área de Direito tributário Internacional, 1996.</li>
                <li>Entre 1990 e 1991, advogada da <b>BRAGA & MARAFON ADVOGADOS ASSOCIADOS</b>.</li>
                <li>Entre 1988 a 1990, consultora júnior e plena, <b>DA KPMG PEAT MARWICK</b>, atuando no contencioso fiscal e administrativo, contratos, societário com ênfase em  fusões, cisões aquisições.</li>
                <li>Estágios profissionais desde 1985: Advocacia Aldo Raia, Depto. Jurídico da Alcoa Alumínio S/A, Hlavnicka, Araújo e Thiollier advogados.</li>
            </ul>
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
b {
    color: white;
}
h5 {
    font-size: 1.6vh;
}
h5:first-of-type {
    margin-top: 5vh;
}
ul {
    font-family: var(--esteban);
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
