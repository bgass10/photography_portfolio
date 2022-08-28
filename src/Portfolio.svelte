<script>
  import Icon from "@iconify/svelte";
  export let catObj;

  const toggeleSelected = (category) => {
    for (const key in catObj) {
      if (key == category) {
        catObj[key].selected = true;
      } else {
        catObj[key].selected = false;
      }
    }
  };
</script>

<section id="portfolio">
  <div class="row">
    {#each Object.entries(catObj) as [k, v]}
      <h1 on:click={() => toggeleSelected(k)} class={catObj[k].selected}>
        {k}
      </h1>
    {/each}
  </div>
  <div class="gallery">
    {#each Object.entries(catObj) as [k, v]}
      {#if catObj[k].selected == true}
        {#each catObj[k].list as photo}
          <a target="_blank" href={photo.url}>
            <div class={photo.orientation + " container"}>
              <img src={photo.url} alt="" />
              <div class="overlayThru" />
              <div class="overlay">
                <Icon icon="carbon:view" color="white" height="36" />
              </div>
            </div>
          </a>
        {/each}
      {/if}
    {/each}
  </div>
  <p>
    Made by <a target="_blank" href="https://brendangass.com/">Brendan Gass</a>
  </p>
</section>

<style>
  .row {
    display: flex;
    flex-direction: row;
    justify-content: center;
    margin-right: 50px;
    margin-left: 50px;
    flex-wrap: wrap;
  }
  .gallery {
    display: flex;
    flex-direction: row;
    margin-left: 80px;
    margin-right: 80px;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
  }
  h1 {
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 32px;
    color: white;
    margin-top: 40px;
    margin-bottom: 50px;
    padding: 30px;
  }
  h1:hover {
    cursor: pointer;
  }
  .v {
    width: 255px;
    height: 375px;
  }
  .h {
    width: 375px;
    height: 255px;
  }
  .s {
    width: 315px;
    height: 315px;
  }
  .container {
    margin-bottom: 30px;
    margin-left: 15px;
    margin-right: 15px;
  }
  img {
    width: 100%;
    height: 100%;
  }
  .true {
    text-decoration: underline;
  }
  p {
    font-family: "Montserrat";
    font-size: 18px;
    text-align: center;
    color: white;
    padding-top: 30px;
    padding-bottom: 30px;
  }
  a {
    color: #fe5099;
  }
  .overlayThru {
    transform: translateY(-101%);
    height: 101.2%;
    width: 100%;
    opacity: 0;
    transition: 0.3s ease;
    background-color: #292736;
  }
  .overlay {
    transform: translateY(-200%);
    height: 100%;
    width: 100%;
    opacity: 0;
    transition: 0.5s ease;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .container:hover .overlayThru {
    opacity: 0.7;
  }
  .container:hover .overlay {
    opacity: 1;
  }
</style>
