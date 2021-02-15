<script>
  import Modal from "./Modal.svelte";
  import Painike from "./Painike.svelte";
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  export let nimi = "";
  export let kuvaus = "";
  export let omistaja = "";

  function tallennaTiedot() {
    dispatch("uusielain", { nimi: nimi, kuvaus: kuvaus, omistaja: omistaja });
  }
</script>

<Modal
  ><h1 slot="header">Uusi Lemmikki</h1>
  <div>
    <label>
      Nimi
      <br /><input type="text" bind:value={nimi} />
    </label>
    <label>
      Kuvaus
      <br /><input type="text" bind:value={kuvaus} />
    </label>
    <label>
      Omistaja
      <br /><input type="text" bind:value={omistaja} />
    </label>
  </div>

  <div slot="footer">
    <Painike on:click={tallennaTiedot}>Tallenna</Painike>
    <Painike on:click={() => dispatch("peruuta")}>Peruuta</Painike>
  </div>
</Modal>
