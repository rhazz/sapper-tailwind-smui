<script>
  import Nav from "../components/Nav.svelte";

  export let segment;
</script>

<style>
  main {
    position: relative !important;
    max-width: 56em !important;
    background-color: white !important;
    padding: 2em !important;
    margin: 0 auto !important;
    box-sizing: border-box !important;
  }
</style>

<Nav {segment} />

<main>
  <slot />
</main>
