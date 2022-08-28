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
      <h6>ABOUT</h6>
      <h5>ME.</h5>
    </div>
  </div>
  <div class="shiftUp">
    <div class="photo">
      <img
        src="https://live.staticflickr.com/65535/51985861255_58a1599f6a_z.jpg"
        alt="Mikayla"
      />
      <div class="imgBorder" />
    </div>
    <div style="text-align: center;">
      <div style="display: inline-block; text-align: left;">
        <h1>Hello! My name is Mikayla.</h1>
        <h3>
          I am a student studying public relations with a<br />minor in
          photography at Penn State.
        </h3>
        <h2>Relevant Experience</h2>
        <div class="textRow">
          <h4>CommAgency</h4>
          <p class="h7">State College, PA</p>
        </div>
        <div class="textRow">
          <p class="title">Photographer</p>
          <p class="h7">2022 - Present</p>
        </div>
        <ul>
          <li>
            Captured over 1,000 professional headshots for Penn State clients.
          </li>
          <li>
            Edited photos in Adobe Photoshop and Adobe Lightroom to <br /> meet given
            specifications.
          </li>
        </ul>
      </div>
    </div>
  </div>
</main>

<style>
  .shiftUp {
    transform: translateY(-150px);
  }
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
  h5 {
    font-family: "Bebas Neue";
    font-weight: 400;
    font-size: 120px;
    color: #fe5099;
    line-height: 85px;
    margin: 0;
  }
  h6 {
    font-family: "Bebas Neue";
    font-weight: 400;
    font-size: 64px;
    color: #ff72ad;
    margin: 0;
  }
  .photo {
    width: 204px;
    height: 300px;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  img {
    width: 100%;
    height: 100%;
  }
  .imgBorder {
    transform: translate(3px, -98%);
    width: 100%;
    height: 100%;
    border: 3px solid #fe5099;
  }
  .textRow {
    display: flex;
    flex-direction: row;
    align-items: baseline;
    justify-content: space-between;
  }
  h1 {
    font-family: "Montserrat";
    color: #fe5099;
    font-size: 48px;
    margin-bottom: 0px;
  }
  h3 {
    font-family: "Montserrat";
    color: white;
    font-size: 27px;
    margin-top: 5px;
  }
  h2 {
    font-family: "Montserrat";
    font-size: 32px;
    color: #ff72ad;
    text-decoration: underline;
    margin-bottom: 5px;
    margin-top: 40px;
  }
  h4 {
    font-family: "Montserrat";
    color: white;
    font-size: 24px;
    margin-bottom: 5px;
    margin-top: 0;
  }
  .h7 {
    font-family: "Montserrat";
    color: white;
    font-size: 24px;
    margin-top: 0;
    margin-bottom: 5px;
  }
  .title {
    font-family: "Montserrat";
    color: white;
    font-size: 24px;
    margin-top: 0;
    font-style: italic;
    margin-bottom: 0;
  }
  li {
    font-family: "Montserrat";
    color: white;
    font-size: 20px;
    margin-top: 10px;
  }
  ul {
    margin-top: 0;
  }
</style>
