<script>
  export let fv = 0;
  export let rate = 0;
  export let years = 0;
  export let frequency = 0;
  export let result = "";
  function handleClick() {
    let res = fv / (1 + rate / (100 * frequency)) ** (frequency * years);
    result = res.toFixed(4);
  }
</script>

<style type="text/css">
  @import "../styles/FinanceStyle.css";
</style>

<div class="financecontent">
  <h2 class="heading">Present Value Calculator</h2>
  <form class="myForm">
    <label class="formChild">
      Future Value:
      <br />
      <input type="text" pattern="^\d*\.?\d*$" bind:value={fv} />
    </label>
    <label class="formChild">
      Annual Compounding Rate:
      <br />
      <input type="text" pattern="^\d*\.?\d*$" bind:value={rate} />
      %
    </label>
    <label class="formChild">
      Compounding Frequency Per Year:
      <br />
      <input type="text" pattern="^\d*\.?\d*$" bind:value={frequency} />
    </label>
    <label class="formChild">
      Years:
      <br />
      <input type="text" pattern="^\d*\.?\d*$" bind:value={years} />
    </label>

    <div id="res" class="formChild">
      Present Value: {result === 'NaN' ? '' : result === '' ? '' : result}
    </div>

    <button on:click|preventDefault={handleClick} class="submitButtonFinance">
      Submit
    </button>
  </form>

</div>
