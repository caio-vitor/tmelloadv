<template>
    <li>
        <span>
            <svg width="10" height="10">
                <rect width="10" height="10" style="fill: var(--cinza-3);"/>
            </svg>
        </span>
        <a :href="link">{{ tipo }}</a>
    </li>
</template>

<script>
export default {
  name: "Button",
  props: {
      tipo: String,
      link: String
  }
}
</script>

<style scoped>
span {
    margin-right: 10px;
}
a, a:visited {
    text-decoration: none;
    color: var(--cinza-3);
    transition: all 0.7s ease;
    padding-bottom: 5px;
}
a:hover {
    color: white;
    border-bottom: 2px solid var(--vermelho);
}
</style>
