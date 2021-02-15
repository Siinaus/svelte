<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  import Painike from "./Painike.svelte";
  export let nimi;
  export let kuvaus;
  export let omistaja;
  export let laji;
  export let haku;

  const poista = () => dispatch("poista", nimi);
</script>

<article>
  <header>
    <h1>{laji} {nimi}</h1>
    <p class="omistaja">{omistaja}</p>
  </header>
  <img src="https://loremflickr.com/320/240/{haku}" alt={nimi} />
  <p>{kuvaus}</p>

  <footer>
    <Painike on:click={poista}>Poista</Painike>
  </footer>
</article>

<style>
  article {
    border: 1px solid black;
    margin: 2em 0;
    box-shadow: 0px 5px 10px #ccc;
    background-color: #eeeeee;
  }

  .omistaja {
    font-size: 0.75em;
  }
</style>
