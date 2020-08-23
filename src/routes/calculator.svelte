<script>
  import NavigationBar from "../components/NavigationBar.svelte";
  import CAGRCalculator from "../components/CAGR.svelte";
  import FVCalculator from "../components/FVCalculator.svelte";
  import PVCalculator from "../components/PVCalculator.svelte";

  export let active = "0";
  export let tabItems = [
    { id: 0, value: "CAGR Calculator" },
    { id: 1, value: "FV Calculator" },
    { id: 2, value: "PV Calculator" },
  ];
  function handleClick(event) {
    active = event.target.id;
  }
</script>

<style type="text/css">
  @import "../styles/HomeFinanceStyle.css";
</style>

<svelte:head>
  <title>Financial Calculators</title>
</svelte:head>

<body class="homePageFinance">
  <!-- <NavigationBar /> -->
  <div class="homeFinanceContainer">

    <div class="navTab">
      {#each tabItems as tabItem}
        <button class="tabItem" id={tabItem.id} on:click={handleClick}>
          {tabItem.value}
        </button>
      {/each}
    </div>

    <div class="tabPanel">
      {#if active === '0'}
        <CAGRCalculator />
      {:else if active === '1'}
        <FVCalculator />
      {:else if active === '2'}
        <PVCalculator />
      {:else}Please select from left bar{/if}

    </div>
  </div>
</body>
