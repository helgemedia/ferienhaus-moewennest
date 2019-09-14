<script>
  import { onMount } from "svelte";
  import { tns } from "tiny-slider/src/tiny-slider";
  import Icon from "fa-svelte";
  import { faArrowLeft } from "@fortawesome/free-solid-svg-icons/faArrowLeft";
  import { faArrowRight } from "@fortawesome/free-solid-svg-icons/faArrowRight";

  let arrowLeft = faArrowLeft;
  let arrowRight = faArrowRight;

  onMount(() => {
    const slider = tns({
      container: ".slider",
      slideBy: "page",
      nav: false,
      controlsContainer: "#customize-controls"
    });
  });
</script>

<style>
  #amenities {
    margin: 0 20px 20px 20px;

    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }

  .amenities-text {
    margin: 10px;

    font-family: "Times New Roman", Times, serif;
    font-size: 20px;
    font-weight: 400;
    word-spacing: 2px;
    line-height: 30px;
  }

  .slider-wrapper {
    margin: 10px;
    width: calc(100% - 20px);
  }

  .slide {
    height: 300px;
  }

  img {
    height: 100%;
  }

  p {
    margin-bottom: 20px;
  }

  ul {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    list-style: none;
  }

  li {
    padding-top: 20px;
    cursor: pointer;
  }

  div :global(.arrow) {
    font-size: 30px;
  }

  @media screen and (min-width: 800px) {
    .amenities-text {
      box-sizing: border-box;
      margin: 0;
      padding: 10px;
      width: 50%;
    }

    .slider-wrapper {
      box-sizing: border-box;
      margin: 0;
      padding: 10px;
      width: 50%;
    }

    .slide {
      height: 500px;
    }
  }

  a.anchor {
    display: block;
    position: relative;
    top: -200px;
    visibility: hidden;
  }
</style>

<a class="anchor" id="amenities-anchor" />

<div id="amenities">
  <div class="amenities-text">
    <p>
      Unser 62 qm großes Ferienhaus wurde im Juni 2018 fertiggestellt.  Es hat
      zwei Schlafzimmer, ein Badezimmer und eine offene Wohnküche,  die mit
      allem ausgestattet ist was einen angenehmen Urlaub gewährleistet.
    </p>
    <p>
      In jedem Schlafzimmer, sowie im Wohnzimmer befindet sich ein Fernseher.
       Die Küche ist mit einem Backofen, einem Ceran-Kochfeld, einer Mikrowelle,
       Toaster, Kaffeemaschine sowie einer Spülmaschine versehen.  In der Küche
      ist außerdem eine Kühl- Gefrierkombination mit großem  Kühlschrank und 3
      Gefrierschubladen.
    </p>
    <p>
      Die große Dusche mit Regendusche macht das Badezimmer zu einer  Wellness
      Oase. Für Ihre Wäsche ist eine Waschmaschine, ein Bügelbrett  und
      Bügeleisen vorhanden. Für Ihren Hund haben wir Hundenäpfe und ein
       Hundekörbchen (geeignet für kleine bis mittelgroße Hunde).
    </p>
    <p>
        Im Wohnzimmer gibt es Bücher und Spiele für Erwachsene und Kinder sowie
       Hörbücher. Sollte das Wetter einmal nicht so gut sein, backen oder kochen
      sie  doch etwas Schönes mit Ihrem Schatz und Ihren Kindern.  Im
      Abstellraum finden Sie übrigens ein Waffeleisen. Eine Waffel mit
      Vanilleeis  und einer leckeren Tasse Tee schmeckt immer und versüßt einen
      verregneten  Nachmittag.
    </p>
    <p>
        Meist ist aber Regen an der Nordsee so schnell verschwunden wie er
      gekommen  ist. An allen Fenstern befinden sich außen elektrische Rollos
      zur Verdunklung  der Räume. Im Außenbereich befinden sich zwei Terrassen,
      so dass Sie die Sonne  zu jeder Tageszeit nutzen können. Ein Tisch mit 6
      Stühlen sowie zwei Sonnenliegen  machen das Ganze komplett.
    </p>
  </div>
  <div class="slider-wrapper">
    <div class="slider">
      <div class="slide">
        <img src="/images/slide-1.jpg" alt="Ferienhaus Möwennest Wohnzimmer" />
      </div>
      <div class="slide">
        <img src="/images/slide-2.jpg" alt="Ferienhaus Möwennest Küche" />
      </div>
      <div class="slide">
        <img src="/images/slide-3.jpg" alt="Ferienhaus Möwennest Bad" />
      </div>
      <div class="slide">
        <img src="/images/slide-4.jpg" alt="Ferienhaus Möwennest Esszimmer" />
      </div>
    </div>

    <ul
      class="controls"
      id="customize-controls"
      aria-label="Carousel Navigation"
      tabindex="0">
      <li
        class="prev"
        data-controls="prev"
        aria-controls="customize"
        tabindex="-1">
        <Icon class="arrow" icon={faArrowLeft} />
      </li>
      <li
        class="next"
        data-controls="next"
        aria-controls="customize"
        tabindex="-1">
        <Icon class="arrow" icon={faArrowRight} />
      </li>
    </ul>
  </div>
</div>
