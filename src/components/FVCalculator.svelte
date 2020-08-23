<script>
  export let pv = 0;
  export let rate = 0;
  export let years = 0;
  export let frequency = 0;
  export let result = "";
  function handleClick() {
    let res = pv * (1 + rate / (frequency * 100)) ** (frequency * years);
    result = res.toFixed(4);
  }
</script>

<style type="text/css">
  @import "../styles/FinanceStyle.css";
</style>

<div class="financecontent">
  <h2 class="heading">Future Value Calculator</h2>
  <form class="myForm">
    <label class="formChild">
      Present Value:
      <br />
      <input type="text" pattern="^\d*\.?\d*$" bind:value={pv} />
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
      Future Value: {result === 'NaN' ? '' : result === '' ? '' : result}
    </div>

    <button on:click|preventDefault={handleClick} class="submitButtonFinance">
      Submit
    </button>
  </form>

</div>
