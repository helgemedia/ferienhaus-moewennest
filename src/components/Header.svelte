<script>
  import { onMount } from "svelte";
  import Nav from "./Nav.svelte";

  let scrolled = false;

  onMount(() => {
    window.onscroll = function() {
      scrollFunction();
    };
  });

  function scrollFunction() {
    if (
      document.body.scrollTop > 50 ||
      document.documentElement.scrollTop > 50
    ) {
      scrolled = true;
    } else {
      scrolled = false;
    }
  }
</script>

<style>
  @import "/main.css";

  #header {
    position: fixed;
    top: 0;
    width: 100%;
    background: #fff;

    z-index: 10;
  }

  h1 {
    margin: 40px 0;
    color: #333;
    text-align: center;
    font-family: "Didot", serif;
    font-size: 12vw;
    font-weight: 100;
    text-transform: uppercase;

    transition: all 0.2s;
  }

  .scrolled {
    font-size: 10vw;
    margin: 40px 0 20px 0;
  }

  @media screen and (min-width: 800px) {
    h1 {
      font-size: 112px;
    }

    .scrolled {
      font-size: 76px;
    }
  }
</style>

<div id="header">
  <h1 class={scrolled ? 'scrolled' : ''}>Möwennest</h1>

  <Nav {scrolled} />
</div>
