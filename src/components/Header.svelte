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

  .waves {
    display: none;
  }

  @media screen and (min-width: 800px) {
    h1 {
      font-size: 80px;
    }

    .scrolled {
      font-size: 50px;
    }

    .waves {
      display: block;
      position: fixed;
      top: 28%;
      right: 50px;
      z-index: -1;

      width: 50%;
    }
  }
</style>

<div id="header">
  <h1 class={scrolled ? 'scrolled' : ''}>Möwennest</h1>

  <Nav {scrolled} />

</div>

<img class="waves" src="/images/waves.svg" alt="waves" />
