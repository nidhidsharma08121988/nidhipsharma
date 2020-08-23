<script>
  import Nav from "../components/Nav.svelte";

  export let segment;
</script>

<style type="text/css" >
  @import "../styles/NavigationBarStyle.css";
</style>

<Nav {segment} />

<body>
  <slot />
</body>
