<style>
  @import "/main.css";

  #nav {
    margin: 0 30px 40px 30px;
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

  li:last-child {
    padding: 0;
  }

  @media screen and (min-width: 800px) {
    #nav {
      margin: 0 20px 40px 20px;
    }

    a {
      font-size: 36px;
    }
  }
</style>

<div id="nav">
  <ul>
    <li>
      <a href="#home">Home</a>
    </li>
    <li>
      <a href="#amenities">Ausstattung</a>
    </li>
    <li>
      <a href="#location">Lage</a>
    </li>
    <li>
      <a href="#contact">Kontakt & Buchung</a>
    </li>
  </ul>
</div>
