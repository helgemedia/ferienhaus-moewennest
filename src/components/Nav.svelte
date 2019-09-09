<script>
  export let scrolled;
</script>

<style>
  @import "/main.css";

  #nav {
    margin: 0 30px 20px 30px;
  }

  li {
    display: inline;
    list-style: none;
    padding-right: 40px;
  }

  a {
    font-family: "Didot", serif;
    font-size: 7vw;
    font-weight: 400;
    text-transform: uppercase;
    text-decoration: none;
    color: black;
    white-space: nowrap;
  }

  a:hover {
    color: #7798a8;
  }

  li:last-child {
    padding: 0;
  }

  .scrolled-link {
    font-size: 5vw;
    line-height: 6vw;
  }

  @media screen and (min-width: 800px) {
    #nav {
      margin: 0 30px 40px 30px;
    }

    .scrolled {
      margin: 0 30px 0 30px !important;
    }

    a {
      font-size: 36px;
      line-height: 40px;
    }

    .scrolled-link {
      font-size: 26px;
    }
  }
</style>

<div id="nav" class={scrolled ? 'scrolled' : ''}>
  <ul>
    <li>
      <a class={scrolled ? 'scrolled-link' : ''} href="#home">Home</a>
    </li>
    <li>
      <a class={scrolled ? 'scrolled-link' : ''} href="#amenities">
        Ausstattung
      </a>
    </li>
    <li>
      <a class={scrolled ? 'scrolled-link' : ''} href="#location">Lage</a>
    </li>
    <li>
      <a class={scrolled ? 'scrolled-link' : ''} href="#contact">
        Kontakt & Buchung
      </a>
    </li>
  </ul>
</div>
