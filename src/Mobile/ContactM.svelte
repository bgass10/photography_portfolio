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
  </div>
  <div style="margin-top: 20vh; text-align: center;">
    <div class="pad">
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
    margin-left: 30px;
    margin-top: 30px;
  }
  .icon:hover {
    opacity: 80%;
    cursor: pointer;
  }
  .pad {
    margin-left: 30px;
    margin-right: 30px;
  }
  h3 {
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 32px;
    color: #fe5099;
    text-align: center;
    margin-top: 7vh;
    padding-bottom: 0;
    margin-bottom: 0;
  }
  h4 {
    font-family: "Montserrat";
    font-size: 18px;
    color: #ff72ad;
    margin-left: 10px;
  }
  p {
    font-family: "Montserrat";
    font-weight: 600;
    font-size: 20px;
    color: white;
    padding: 0;
    margin: 0;
    margin-top: 15px;
  }
  .emailRow {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
</style>
