<script>
  import Icon from "@iconify/svelte";
  export let page;
</script>

<div class="bg">
  <div class="wrapper" on:click={() => (page = "home")}>
    <Icon icon="ri:close-fill" color="#292736" height="28" />
  </div>
  <div class="nav">
    <h1 on:click={() => (page = "about")}>ABOUT</h1>
    <h1 on:click={() => (page = "contact")}>CONTACT</h1>
  </div>
</div>

<style>
  .bg {
    position: absolute;
    top: 0;
    background-color: #fe5099;
    width: 100vw;
    height: 100vh;
  }
  .wrapper {
    position: absolute;
    top: 0;
    width: 28px;
    height: 28px;
    margin-top: 3.7vh;
    margin-left: 84.5vw;
  }
  .nav {
    position: absolute;
    top: 4vh;
    right: 12vw;
  }
  h1 {
    color: #292736;
    font-family: Montserrat;
    font-size: 10vw;
    margin-top: 0;
    margin-bottom: 0.9vh;
  }
</style>
