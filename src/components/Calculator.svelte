<script>
  let data = {
    weight: null,
    height: null,
  };

  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  const calculate = () => {
    dispatch("calculate", data);
  };

  const reset = () => {
    data = {
      weight: null,
      height: null,
    };
    dispatch("reset");
  };
</script>

<div class="bmi-calculator">
  <div class="inputs">
    <div>
      <span>Weight (kg) : </span>
      <input type="number" bind:value={data.weight} />
    </div>
    <div>
      <span>Height (cm) : </span>
      <input type="number" bind:value={data.height} />
    </div>
  </div>
  <div class="options">
    <button class="btn" style="background-color:#007bff" on:click={calculate}
      >Calculate</button
    >
    <button class="btn" style="background-color: #dc3545;" on:click={reset}
      >Reset</button
    >
  </div>
</div>

<style lang="scss">
  .btn {
    background-color: #44c767;
    border-radius: 2px;
    /* border: 1px solid grey; */
    display: inline-block;
    cursor: pointer;
    color: #ffffff;
    font-family: Arial;
    font-size: 18px;
    padding: 11px 76px;
    text-decoration: none;
    /* text-shadow: 0px 0px 0px #2f6627; */
    max-width: 200px;
  }
  .btn:hover {
    background-color: #5cbf2a;
  }
  .btn:active {
    position: relative;
    top: 1px;
  }

  .bmi-calculator {
    margin-top: 5%;
  }

  .inputs {
    display: flex;
    align-items: center;
    flex-direction: column;

    span {
      font-size: 16px;
      font-weight: bold;
    }
  }

  .options {
    margin-top: 5%;
    display: flex;
    justify-content: center;
    button:nth-child(1) {
      margin-right: 10px;
    }
    button:nth-child(2) {
      margin-left: 10px;
    }
  }
</style>
