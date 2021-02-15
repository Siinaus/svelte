<script>
  const info = [
    "Muista ruokkia säännöllisesti",
    "Huolehdi sopivista virikkeistä",
    "Käytä lääkärissä tarvittaessa",
    "Ulkoiluta säännöllisesti",
  ];

  let i = 0;

  export let nakyvyysAika = 3000;

  setInterval(() => {
    i = i < info.length - 1 ? i + 1 : 0;
  }, nakyvyysAika);

  $: vinkki = info[i];
</script>

<div>
  <p class="vihje">
    {vinkki}
  </p>
</div>

<style>
  .vihje {
    font-size: 2em;
  }
</style>
