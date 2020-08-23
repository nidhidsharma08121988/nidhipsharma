<script>
  // export let selectedMenuItem;
  export let navMenuItems = [
    {
      id: 0,
      value: "Home",
      link: ".",
      target: "",
    },
    {
      id: 1,
      value: "Reader's Delight",
      link: "https://shortstoriesbynidhi.home.blog/",
      target: "_blank",
    },
    {
      id: 2,
      value: "Cook Book",
      link: "https://vegetarianhealthy.food.blog/",
      target: "_blank",
    },
    {
      id: 3,
      value: "Financial Calculators",
      link: "finance",
      target: "",
    },
  ];
</script>

<style lang="Scss">
  @import "../ScssStyles/NavigationBarStyle.scss";
</style>

<div class="navigation">
  {#each navMenuItems as menuItem}
    <a
      class="navItem"
      id={menuItem.id}
      href={menuItem.link}
      target={menuItem.target}>
      {menuItem.value}
    </a>
  {/each}
</div>
