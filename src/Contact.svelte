<script>
  export let page;
  import Icon from "@iconify/svelte";
</script>

<main>
  <div class="row">
    <div
      on:click={() => {
        page = "home";
      }}
      class="icon"
    >
      <Icon
        class="arrow"
        icon="carbon:arrow-left"
        color="#fe5099"
        height="36"
      />
    </div>
    <div class="emblem">
      <h2>GET IN</h2>
      <h1>TOUCH</h1>
    </div>
  </div>
  <div style="text-align: center;">
    <div>
      <h3>I would love to work with you!</h3>
      <p>
        I am currently accepting clients in the<br />central Pennsylvania area.
        Shoot me<br />an email for addition information!
      </p>
    </div>
    <div class="emailRow">
      <Icon class="email" icon="carbon:email" color="#ff72ad" height="38" />
      <h4>mikaylagebhart15@gmail.com</h4>
    </div>
  </div>
</main>

<style>
  .row {
    display: flex;
    flex-direction: row;
  }
  .icon {
    margin-left: 50px;
    margin-top: 50px;
  }
  .icon:hover {
    opacity: 80%;
    cursor: pointer;
  }
  .emblem {
    margin-left: 30px;
    margin-top: 50px;
  }
  h1 {
    font-family: "Bebas Neue";
    font-weight: 400;
    font-size: 72px;
    color: #fe5099;
    line-height: 40px;
    margin: 0;
  }
  h2 {
    font-family: "Bebas Neue";
    font-weight: 400;
    font-size: 74px;
    color: #ff72ad;
    margin: 0;
  }
  h3 {
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 46px;
    color: #fe5099;
    text-align: center;
    margin-top: 7vh;
    padding-bottom: 0;
    margin-bottom: 0;
  }
  h4 {
    font-family: "Montserrat";
    font-size: 28px;
    color: #ff72ad;
    margin-left: 10px;
  }
  p {
    font-family: "Montserrat";
    font-weight: 600;
    font-size: 37px;
    color: white;
    padding: 0;
    margin: 0;
  }
  .emailRow {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
</style>
