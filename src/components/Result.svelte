<script>
  import Info from "./Info.svelte";
  export let result;
  export let value = "";
</script>

<div class="bmi-result">
  <div>{result}</div>
  <div>{value}</div>
  <Info />
</div>

<style lang="scss">
  .bmi-result {
    margin-top: 5%;
    div {
      display: flex;
      justify-content: center;
      font-size: 20px;
      font-weight: bold;
    }
  }
</style>
