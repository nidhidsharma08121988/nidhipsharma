<script>
  import Nav from "../components/Nav.svelte";

  export let segment;
</script>

<style lang="Scss">
  @import "../ScssStyles/HomeStyle.scss";
</style>

<Nav {segment} />

<body>
  <slot />
</body>
