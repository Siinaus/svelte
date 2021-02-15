<script>
  import Elain from "./Elain.svelte";
  export let lemmikit;
  export let elain;
</script>

{#each lemmikit as lemmikki}
  <Elain {...lemmikki} {...elain} on:poista />
{/each}
