<script lang="ts">
  import NachoLogo from "$lib/NachoLogo.svelte";
</script>

<style lang="scss">
  .container {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    text-align: center;
  }
</style>

<div class="container">
  <div style="padding:40px 0px">
    <h1>Welcome to the NACHO token</h1>
    <h3>
      Wrap tokens from other blockchains <br /> to use on the Tezos blockchain
      <br /> and earn NACHO tokens
    </h3>
  </div>
  <NachoLogo nachoColorLeft="#f7931a" nachoColorRight="#0f62ff" />
</div>
