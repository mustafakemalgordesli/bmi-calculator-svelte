<script>
  import Result from "./components/Result.svelte";
  import Calculator from "./components/Calculator.svelte";
  let result = "";
  let value = "";

  const calculate = (e) => {
    console.log(e);
    let data = e.detail;
    if (data.weight == null && data.height == null) {
      result = "Input field must not be empty!";
      return;
    }
    result = (data.weight / Math.pow(data.height / 100, 2)).toFixed(2);
    if (result < 18.5) value = "Under Weight";
    else if (result <= 25) value = "Normal";
    else if (result <= 30) value = "Over Weight";
    else if (result > 30) value = "Obese";
  };

  const reset = () => {
    result = "";
    value = "";
  };
</script>

<div class="container">
  <div class="bmi-box">
    <h1 class="title">BMI Calculator</h1>
    <Calculator on:calculate={calculate} on:reset={reset} />
    <Result {result} {value} />
  </div>
</div>

<style>
  .container {
    max-width: 720px;
    height: 650px;
    margin-left: auto;
    margin-right: auto;
    background-color: lightcoral;
    margin-top: 40px;
    border-radius: 10px;
    border: 1px solid grey;
  }

  .bmi-box {
    display: flex;
    flex-direction: column;
  }

  .title {
    margin-top: 5%;
    margin-left: auto;
    margin-right: auto;
  }
</style>
