<script>
  import Icon from "@iconify/svelte";
  export let page;
</script>

<main>
  <div class="wrapper" on:click={() => (page = "nav")}>
    <Icon class="icon" icon="ri:menu-5-fill" color="white" height="28" />
  </div>
  <div class="col">
    <div class="textBox">
      <h1>MIKAYLA<br />GEBHART</h1>
      <h3>PHOTOGRAPHER</h3>
    </div>
  </div>
</main>

<style>
  main {
    height: 40vh;
    background-color: #fe5099;
  }
  .col {
    display: flex;
    height: 40vh;
    align-items: center;
    justify-content: center;
  }
  .wrapper {
    position: absolute;
    width: 28px;
    height: 28px;
    top: 3.7vh;
    right: 10vw;
  }
  h1 {
    color: white;
    font-family: "Bebas Neue";
    font-size: 15vw;
    text-align: center;
    margin-top: 7vh;
    margin-bottom: 0.6vh;
    line-height: 14vw;
  }
  h3 {
    color: #292736;
    opacity: 75%;
    font-family: "Bebas Neue";
    font-size: 7vw;
    text-align: center;
    margin-left: 14vw;
    margin-right: 14vw;
    margin-top: 0;
  }
</style>
