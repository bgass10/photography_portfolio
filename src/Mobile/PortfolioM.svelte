<script>
  export let catObj;

  let selected = "All";

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

<main>
  <form>
    <select bind:value={selected} on:change={() => toggeleSelected(selected)}>
      {#each Object.entries(catObj) as [k, v]}
        <option value={k}>
          {k}
        </option>
      {/each}
    </select>
  </form>
  <div class="gallery">
    {#each Object.entries(catObj) as [k, v]}
      {#if catObj[k].selected == true}
        {#each catObj[k].list as photo}
          <a target="_blank" href={photo.url}>
            <img class={photo.orientation} src={photo.url} alt="" />
          </a>
        {/each}
      {/if}
    {/each}
  </div>
  <p>
    Made by <a target="_blank" href="https://brendangass.com/">Brendan Gass</a>
  </p>
</main>

<style>
  .gallery {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  img {
    margin-top: 20px;
  }
  .v {
    width: 61.5vw;
    height: 90vw;
  }
  .h {
    width: 90vw;
    height: 61.5vw;
  }
  .s {
    width: 315px;
    height: 315px;
  }
  select {
    background-color: transparent;
    border: none;
    color: #fe5099;
    width: max-content;
    background: #292736;
    margin-left: 30px;
    margin-top: 20px;
  }
  option {
    font-family: "Montserrat";
    font-size: 10px;
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
</style>
