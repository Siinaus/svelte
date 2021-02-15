<script>
  import Otsikko from "./Otsikko.svelte";
  import Vinkki from "./Vinkki.svelte";
  import Painike from "./Painike.svelte";
  import Lemmikit from "./Lemmikit.svelte";
  import UusiElain from "./UusiElain.svelte";

  export let lemmikki;

  let elain = {
    haku: "horse",
    laji: "Hevonen",
  };
  let nimi = "";
  let kuvaus = "";
  let omistaja = "";

  function tyhjaaLemmikinTiedot() {
    nimi = "";
    kuvaus = "";
    omistaja = "";
  }

  function lisaaLemikki(event) {
    let uusiLemmikki = {
      nimi: event.detail.nimi,
      kuvaus: event.detail.kuvaus,
      omistaja: event.detail.omistaja,
    };
    console.log(uusiLemmikki);

    lemmikit = [...lemmikit, uusiLemmikki];
    tyhjaaLemmikinTiedot();
  }

  let naytaInputit = false;

  let lemmikit = [
    {
      nimi: "Pörrö",
      kuvaus: "Tuttavallinen ja leikkisä",
      omistaja: "Pekka Pekkanen",
    },
    {
      nimi: "Paavali",
      kuvaus: "Uninen tapaus",
      omistaja: "Eemeli Mäki",
    },
    {
      nimi: "Pikku Myy",
      kuvaus: "Puree kaikkea",
      omistaja: "Ulrik Helm",
    },
  ];

  const poistaLemmikki = (e) => {
    lemmikit = lemmikit.filter((l) => l.nimi !== e.detail);
  };
</script>

<main>
  <Otsikko {lemmikki} />

  <Lemmikit {lemmikit} {elain} on:poista={poistaLemmikki} />

  <Vinkki />

  {#if naytaInputit}
    <UusiElain
      on:peruuta={() => (naytaInputit = false)}
      on:uusielain={lisaaLemikki}
    />
  {/if}

  <Painike on:click={() => (naytaInputit = !naytaInputit)}>Lisää uusi</Painike>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
