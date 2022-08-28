<script>
  import HomeM from "./HomeM.svelte";
  import Navigator from "./Navigator.svelte";
  import PortfolioM from "./PortfolioM.svelte";
  import ContactM from "./ContactM.svelte";
  import AboutM from "./AboutM.svelte";
  export let catObj;
  let page = "home";
</script>

{#if page == "home"}
  <HomeM bind:page />
  <PortfolioM {catObj} />
{:else if page == "nav"}
  <Navigator bind:page />
{:else if page == "about"}
  <AboutM bind:page />
{:else if page == "contact"}
  <ContactM bind:page />
{/if}
