<script>
  //... 3 dots for going out of this folder thrice
  export let initVal = 0;
  export let finalVal = 0;
  export let years = 0;
  export let result = "";

  function handleClick() {
    let res = ((finalVal / initVal) ** (1 / years) - 1) * 100;
    result = res.toFixed(4);
  }
</script>

<style type="text/css">
  @import "../styles/FinanceStyle.css";
</style>

<div class="financecontent">
  <h2 class="heading">CAGR Calculator</h2>
  <form class="myForm">
    <label class="formChild">
      Initial Value:
      <br />
      <input type="text" pattern="^\d*\.?\d*$" bind:value={initVal} />
    </label>
    <label class="formChild">
      Final Value:
      <br />
      <input type="text" pattern="^\d*\.?\d*$" bind:value={finalVal} />
    </label>
    <label class="formChild">
      Years:
      <br />
      <input type="text" pattern="^\d*\.?\d*$" bind:value={years} />
    </label>
    <div id="res" class="formChild">
      CAGR: {result === 'NaN' ? '' : result === '' ? '' : result + '%'}
    </div>

    <button on:click|preventDefault={handleClick} class="submitButtonFinance">
      Submit
    </button>
  </form>
</div>
