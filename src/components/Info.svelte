<script></script>

<div class="bmi-info">
  <div>
    <p>&#60; 18.5</p>
    <p>Under Weight</p>
  </div>
  <div>
    <p>18.5 - 25</p>
    <p>Normal</p>
  </div>
  <div>
    <p>25 -30</p>
    <p>Over Weight</p>
  </div>
  <div>
    <p>&#62; 30</p>
    <p>Obese</p>
  </div>
</div>

<style lang="scss">
  .bmi-info {
    margin-top: 5%;
    margin-left: auto;
    margin-right: auto;
    display: flex;
    justify-content: space-around;

    div {
      color: white;
      font-size: 16px;
      font-weight: bold;
      border-radius: 10px;
      padding: 20px;
      height: 100px;
      width: 100px;
      background-color: black;
      display: flex;
      flex-direction: column;
      p {
        text-align: center;
      }
    }

    div:nth-child(1) {
      background-color: #007bff;
    }
    div:nth-child(2) {
      background-color: #43a047;
    }
    div:nth-child(3) {
      background-color: #ffc107;
    }
    div:nth-child(4) {
      background-color: #dc3545;
    }
  }
</style>
