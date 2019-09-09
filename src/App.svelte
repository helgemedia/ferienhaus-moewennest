<script>
  import Header from "./components/Header.svelte";
  import Nav from "./components/Nav.svelte";
  import Home from "./components/Home.svelte";
  import Amenities from "./components/Amenities.svelte";
  import Location from "./components/Location.svelte";
  import Contact from "./components/Contact.svelte";
</script>

<style>
  #app {
    max-width: 1920px;
    margin: 0 auto;
  }
</style>

<div id="app">
  <Header />

  <Home />

  <Amenities />

  <Location />

  <Contact />
</div>
