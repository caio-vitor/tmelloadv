<template>
  <div id="contato">
    <div class="fale">
      <h1>Fale Conosco</h1>
    </div>
    <div class="contato-form-wrapper">
      <div class="form">
        <div class="intro">
          <p>Na TMello estamos à disposição para lhe atender!</p>
          <p>Caso deseje consultar-nos, preencha os campos abaixo para entrarmos em contato.</p>
        </div>
        <form action="">
          <input type="text" placeholder="Nome">
          <input type="email" placeholder="E-mail">
          <select name="area-do-problema">
            <option value="" selected>Área do problema</option>
            <option value="">Advocacia Extrajudicial</option>
            <option value="">Mediação e conciliação</option>
            <option value="">Contratos</option>
            <option value="">Família</option>
            <option value="">Interdições</option>
          </select>
          <select name="como-nos-conheceu">
            <option value="" selected>Como nos conheceu</option>
            <option value="">Indicação</option>
            <option value="">Internet</option>
            <option value="">Outros</option>
          </select>
          <button><li>Enviar</li></button>
        </form>
      </div>
      <div class="vl"></div>
      <div class="info">
        <div class="links-uteis">
          <h5>Links úteis</h5>
          <ul>
            <li><a href="http://www.oabsp.org.br/">OAB-SP</a></li>
            <li><a href="http://portal.stf.jus.br">STF</a></li>
            <li><a href="http://www.stj.jus.br/">STJ</a></li>
          </ul>
          <ul>
            <li><a href="http://www12.senado.leg.br/hpsenado">Senado</a></li>
            <li><a href="http://www.congressonacional.leg.br">Congresso Nacional</a></li>
            <li><a href="http://www.cartorio24horas.com.br">Cartório 24h</a></li>
          </ul>
        </div>
        <div class="end">
          <img class="logo-contato" src="@/assets/logo-tm.svg">
          <p>Av. Nove de Julho, 4939 <br> Torre Europa, cj. 16 ‒ CEP 01407-200</p>
          <p>+55 11 3037-7018</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contato'
}
</script>

<style scoped>
#contato {
    width: 100%;
    display: grid;
    grid-template-rows: 12vh 1fr;
}
.fale {
  background-color: var(--cinza-5);
  display: flex;
}
.fale h1 {
  margin: 0;
  margin-left: 10vw;
  text-transform: uppercase;
  color: var(--cinza-2);
  align-self: center;
  font-size: 5vh;
}
.contato-form-wrapper {
  background-color: var(--cinza-3);
  display: grid;
  grid-template-columns: 1fr 10vw 1fr;
  justify-items: start;
  padding: 5vh 0;
  height: 60vh;
}
.form{
  display: grid;
  padding-left: 10vw;
  width: 75%;
  align-items: stretch;
}
.form p {
  font-family: var(--esteban);
  color: var(--cinza-5);
  font-size: 2.5vh;
}
form {
  margin-top: -20vh;
  display: grid;
  align-items: end;
  grid-gap: 2vh;
}
.vl {
  width: 1px;
  height: 100%;
  background-color: var(--cinza-5);
  justify-self: center;
}
.info {
  display: grid;
  align-items: stretch;
  color: var(--cinza-5);
}
h5 {
  font-size: 3vh;
  text-transform: uppercase;
  margin: 0;
  padding: 0;
}
ul {
  padding: 0;
  list-style-type: square;
  list-style-position: inside;
  text-transform: uppercase;
}
ul li {
  margin-bottom: 1.5vh;
}
.end {
  align-self: end;
  font-size: 2vh;
}
.info p {
  font-family: var(--esteban);
}
.logo-contato {
  width: 20vw;
}
input {
  box-shadow: none;
  outline: none;
  border: none;
  background: none; 
  border-bottom: 1px solid var(--cinza-4);
  font-family: var(--mont);
  font-size: 1.75vh;
  color: var(--cinza-4);
}
input::placeholder {
  color: var(--cinza-4);
}
input:focus {
  border-bottom: 2px solid white;
}
select {
  box-shadow: none;
  outline: none;
  border: none;
  background: none; 
  border-bottom: 1px solid var(--cinza-4);
  font-family: var(--mont);
  font-size: 1.75vh;
  color: var(--cinza-4);
  cursor: pointer;
}
button {
  box-shadow: none;
  outline: none;
  border: none;
  background: none; 
  font-family: var(--mont);
  font-size: 1.75vh;
  color: var(--cinza-4);
  cursor: pointer;
  text-transform: uppercase;
  text-align: left;
  transition: all 0.3s ease;
}
button:hover {
  color: white;
}
button li {
  list-style-type: square;
}

.links-uteis {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 5vh 1fr;
}

.links-uteis h5 {
  grid-column: span 2;
  color: var(--camelo);
}
.links-uteis a {
  color:var(--cinza-4);
  text-decoration: none;
  transition: color 0.3s ease;
}
.links-uteis a:visited {
  color: var(--camelo);
}

.links-uteis a:hover {
  color: white;
}
@media (max-width: 768px) {
  #contato{
    grid-template-columns: 1fr;
  }
  .contato-form-wrapper {
    grid-template-columns: 1fr;
    height: 130vh;
  }
  form {
    margin-top: 2vh;
    grid-gap: 4vh;
  }
  input {
    font-size: 2.5vh;
  }
  select {
    font-size: 2.5vh;
    
  }
  button {
    font-size: 2.5vh;
  }
  .form {
    width: 80%;
  }
  .info {
    padding-left: 10vw;
  }
  .vl {
    display: none;
  }
  .end {
    margin-top: 10vh;
    font-size: 2.5vh;
  }
  .logo-contato{
    width: 70vw;
  }
  h5 {
    margin-top: 8vh;
  }
}
</style>

