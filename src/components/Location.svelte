<script>
  import { GoogleMap } from "@beyonk/svelte-googlemaps";

  let mapConfig = {
    center: {
      lat: 53.731008,
      lng: 8.526774
    },
    zoom: 14
  };
</script>

<style>
  #location {
    margin: 0 20px 20px 20px;

    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }

  .location-text {
    margin: 10px;

    font-family: "Times New Roman", Times, serif;
    font-size: 20px;
    font-weight: 400;
    word-spacing: 2px;
    line-height: 30px;
  }

  p {
    margin-bottom: 20px;
  }

  .gmaps-wrapper {
    width: 100%;
    height: 500px;
  }

  @media screen and (min-width: 800px) {
    .location-text {
      box-sizing: border-box;
      margin: 0;
      padding: 10px;
      width: 50%;
    }

    .gmaps-wrapper {
      box-sizing: border-box;
      margin: 0;
      padding: 10px;
      width: 50%;
    }
  }

  a.anchor {
    display: block;
    position: relative;
    top: -200px;
    visibility: hidden;
  }
</style>

<a class="anchor" id="location-anchor" />

<div id="location">
  <div class="location-text">
    <p>
      Der Strand und der Hundestrand befinden sich in etwa 900 m Entfernung  und
      sind zu Fuß in etwa 10 Minuten zu erreichen. In unmittelbarer Nähe unseres
       Ferienhauses ist ein Spielplatz, weitere große und sehr schöne
      Spielplätze sind am Strand.  Dorum Neufeld hat außerdem für Regenwetter
      ein Kinderspielhaus.
    </p>
    <p>
      Das Bad „Watt’n Bad“ mit Freibad (Wellenbad alle halbe Stunde) und
      Hallenbad ist eine  weitere Attraktion vor Ort. In etwa 25 km Entfernung
      finden Sie Cuxhaven und Bremerhaven  mit weiteren Freizeitmöglichkeiten,
      wobei ich Ihnen besonders den „Zoo am Meer“ in  Bremerhaven ans Herz legen
      möchte. Hundebesitzer können den Agility Platz im Ferienpark nutzen.  Den
      Schlüssel bekommen Sie im Hotel.
    </p>
    <p>
      Einkaufsmöglichkeiten gibt es in etwa 500 m Entfernung.  Für größere
      Einkäufe bietet sich Dorum in etwa 5 km Entfernung an.  Hier gibt es Lidl,
      Aldi, Netto und zwei Edeka Märkte.
    </p>
  </div>
  <div class="gmaps-wrapper">
    <GoogleMap
      apiKey="AIzaSyDO_QI_LN-Vx3XBroaHkXz9XELOXgOaJ6U"
      options={mapConfig} />
  </div>
</div>
