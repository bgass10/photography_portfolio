<script>
  import Home from "./Home.svelte";
  import Portfolio from "./Portfolio.svelte";
  import About from "./About.svelte";
  import Contact from "./Contact.svelte";
  import MobileHub from "./Mobile/MobileHub.svelte";
  import { config } from "../config";
  import { initializeApp } from "firebase/app";
  import {
    getFirestore,
    collection,
    onSnapshot,
    doc,
    getDoc,
  } from "firebase/firestore";

  const firebaseApp = initializeApp(config);
  const db = getFirestore();
  const colRef = collection(db, "All Photos");
  const catRef = collection(db, "Categories");

  var catObj = {};

  let categories = [];

  const catUnsubscribe = onSnapshot(catRef, (querySnapshot) => {
    querySnapshot.forEach((doc) => {
      let category = { ...doc.data(), id: doc.id };
      categories = [...categories, category];
    });
    for (let i = 0; i < categories.length; i++) {
      catObj[categories[i].id] = { list: [], selected: false };
    }
  });

  const unsubscribe = onSnapshot(colRef, (querySnapshot) => {
    querySnapshot.forEach((doc) => {
      let photo = { ...doc.data() };
      catObj.All.list = [photo, ...catObj.All.list];
      catObj.All.selected = true;
      catObj[photo.category].list = [photo, ...catObj[photo.category].list];
    });
  });

  let page = "home";
  let width;
  let height;
</script>

<svelte:window bind:outerWidth={width} bind:outerHeight={height} />

<svelte:head>
  <link
    href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Montserrat:wght@600;700&display=swap"
    rel="stylesheet"
  />
</svelte:head>

{#if width > 769 && width > height}
  {#if page == "home"}
    <Home bind:page />
    <Portfolio {catObj} />
  {:else if page == "about"}
    <About bind:page />
  {:else if page == "contact"}
    <Contact bind:page />
  {/if}
{:else}
  <MobileHub {catObj} />
{/if}

<style>
</style>
