<script>
  export let page;
</script>

<main>
  <div class="left">
    <h2>GEBHART PHOTOGRAPHY</h2>
    <div style="text-align: center;">
      <div style="display: inline-block; text-align: left;">
        <h1>MIKAYLA<br />GEBHART</h1>
        <h3>PHOTOGRAPHER</h3>
      </div>
    </div>
  </div>
  <div class="right">
    <div class="Navbar">
      <h4
        on:click={() => {
          page = "about";
        }}
      >
        About Me
      </h4>
      <a href="#portfolio">
        <h4>Portfolio</h4>
      </a>
      <h4
        on:click={() => {
          page = "contact";
        }}
      >
        Contact
      </h4>
    </div>
    <img class="pattern" src="https://i.imgur.com/srKq1Ua.png" alt="pattern" />
  </div>
</main>

<style>
  main {
    display: flex;
    flex-direction: row;
  }
  .pattern {
    position: absolute;
    right: 0;
    bottom: 0;
    height: 85vh;
    width: 50vw;
  }
  .left {
    width: 50vw;
    height: 100vh;
    background-color: #ff72ad;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .right {
    width: 50vw;
    height: 100vh;
    background-color: #ff72ad;
  }
  h1 {
    font-family: "Bebas Neue";
    font-size: 144px;
    color: white;
    font-weight: 400;
    line-height: 125px;
    margin: 0px;
  }
  h2 {
    position: absolute;
    color: white;
    font-family: "Bebas Neue";
    font-weight: 500;
    left: 50px;
    top: 10px;
    font-size: 32px;
  }
  h3 {
    font-family: "Montserrat";
    font-size: 24px;
    font-weight: 700;
    color: #292736;
    padding-top: 0px;
    margin-top: 0px;
  }
  .Navbar {
    display: flex;
    flex-direction: row;
    justify-content: end;
    margin-right: 50px;
    margin-top: 10px;
  }
  h4 {
    font-family: "Montserrat";
    font-weight: 600;
    font-size: 20px;
    color: white;
    margin-left: 50px;
  }
  h4:hover {
    opacity: 80%;
    cursor: pointer;
  }
  a:link {
    text-decoration: inherit;
    color: inherit;
    cursor: auto;
  }

  a:visited {
    text-decoration: inherit;
    color: inherit;
    cursor: auto;
  }
</style>
