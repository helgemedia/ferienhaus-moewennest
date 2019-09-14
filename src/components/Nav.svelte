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
    font-size: 22px;
    font-weight: 400;
    line-height: 26px;
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
    font-size: 20px;
    line-height: 24px;
  }

  @media screen and (min-width: 800px) {
    a {
      font-size: 30px;
      line-height: 40px;
    }

    .scrolled-link {
      font-size: 24px;
    }
  }
</style>

<div id="nav" class={scrolled ? 'scrolled' : ''}>
  <ul>
    <li>
      <a class={scrolled ? 'scrolled-link' : ''} href="#home-anchor">Home</a>
    </li>
    <li>
      <a class={scrolled ? 'scrolled-link' : ''} href="#amenities-anchor">
        Ausstattung
      </a>
    </li>
    <li>
      <a class={scrolled ? 'scrolled-link' : ''} href="#location-anchor">
        Lage
      </a>
    </li>
    <li>
      <a class={scrolled ? 'scrolled-link' : ''} href="#contact-anchor">
        Kontakt & Buchung
      </a>
    </li>
  </ul>
</div>
