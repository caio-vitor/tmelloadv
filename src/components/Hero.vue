<template>
    <div id="hero">
        <img class="logo-hero" src="@/assets/logo-tm.svg">
        <p>Passe o mouse sobre o logo para testar a cor ⬆</p>
        <img class="scroll" src="@/assets/scroll-icon.svg">
    </div>
</template>

<script>
export default {
  name: 'Hero'
}
</script>

<style scoped>
#hero{
    width: 100%;
    height: 100vh;
    background-image: url('../assets/IMG_3886.jpg');
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    display: grid;
    grid-template-rows: 1fr 10vh 1fr;
    align-items: center;
    justify-items: center;
    cursor: pointer;
}
.logo-hero {
    margin-top: 25vh;
    max-width: 80vw;
    transition: all 0.5s ease;
}
.scroll {
    max-width: 25vw;
}
p {
    margin: 0;
    color: white;
}
.logo-hero:hover {
    filter: invert(.8) sepia(.3);
}
</style>
