<script lang="ts">
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<style lang="scss">
  @import "../styles/index.scss";

  main {
    height: 100%;
    width: 100%;
    display: grid;
    grid-template-rows: 10% 85% 5%;
  }
</style>

<main>
  <Header />
  <slot />
  <Footer />
</main>
