<template>
    <div id="hero">
        <img class="logo-hero" src="@/assets/logo-tm.svg">
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
    grid-template-rows: 10vh 1fr 1fr;
    align-items: center;
    justify-items: center;
}
.logo-hero {
    margin-top: 25vh;
    max-width: 30vw;
    grid-row: 2;
}
.scroll {
    max-width: 25vw;
    grid-row: 3;
}
p {
    margin: 0;
    color: white;
}
</style>
