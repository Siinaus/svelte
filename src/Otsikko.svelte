<script>
  export let lemmikki;
</script>

<header>
  <h1>{lemmikki}-info</h1>
  <slot />
</header>

<style>
  header {
    background-color: #909090;
    padding: 2em;
    margin-bottom: 1em;
  }

  h1 {
    text-transform: uppercase;
    color: white;
    text-decoration: underline;
  }

  slot {
    position: fixed;
    right: 1em;
    top: 1em;
  }
</style>
