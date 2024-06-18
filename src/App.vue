<template>
  <div class="wrapper-test-entities">
    <div class="progress-bar" >
      <svg viewBox="0 0 36 36" class="circular-chart">
        <path class="circle-bg"
              d="M18 2.0845
              a 15.9155 15.9155 0 0 1 0 31.831
              a 15.9155 15.9155 0 0 1 0 -31.831"
        />
        <path class="circle"
              d="M18 2.0845
              a 15.9155 15.9155 0 0 1 0 31.831
              a 15.9155 15.9155 0 0 1 0 -31.831"
        />
      </svg>
      <div class="percentage">
        0/7
      </div>
    </div>

    <div class="info">
      <div class="tag">Чеклист</div>
      <div class="progress">Выполнено: 0 из 7 действий</div>
      <div class="next-step">Следующее действие: Созвониться с клиентом до 23.05.24 12:00</div>
    </div>

    <div class="actions">
      <button class="open-check-list">Открыть чеклист</button>
    </div>
  </div>
</template>


<style>

body{
  margin: 0;
}
#app {
  font-family: "Inter", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #444;
  height: 100vh;
}
</style>



<style lang="css" scoped>
.wrapper-test-entities {
  display: flex;
  max-width: fit-content;
  padding: 12px 18px 15px 22px;
  align-items: center;
  border-radius: 10px;
  background-color: #3579F5;
  gap: 16px;
  color: white;


  .progress-bar {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    min-width: 60px;
    min-height: 60px;
    width: 60px;
    height: 60px;
    --percentage: 50; /* Установите здесь значение процента */

    .circular-chart {
      width: 100%;
      height: 100%;
      transform: rotate(0deg);
    }

    .circle-bg {
      fill: none;
      stroke: #fff;
      opacity: 0.5;
      stroke-width: 1px;
    }

    .circle {
      fill: none;
      stroke: #fff;
      stroke-width: 1.6;
      stroke-linecap: round;
      stroke-dasharray: 100;
      stroke-dashoffset: calc(100 - (var(--percentage) * 100 / 100));
      transition: stroke-dashoffset 0.5s ease;
    }

    .percentage {
      position: absolute;
      font-size: 20px;
      line-height: 30px;
      font-weight: 400;
    }
  }

  .info{
    display: flex;
    flex-direction: column;
    width: 441px;
    align-items: start;
    font-weight: 400;
    gap: 4px;
    .tag{
      background-color: #2364DB;
      font-size: 12px;
      line-height: 18px;
      padding: 0 10px;
      border-radius: 40px;
    }

    .progress{
      font-size: 15px;
      font-weight: 600;
      line-height: 20px;
    }

    .next-step{
      font-size: 12px;
      line-height: 18px;
    }
  }

  .actions{
    display: flex;

    .open-check-list{
      color: #4777ED;
      background-color: #F4F8FF;
      border: none;
      width: 170px;
      font-size: 14px;
      font-weight: 400;
      line-height: 20px;
      border-radius: 6px;
      padding: 10px 25px;
      white-space: nowrap;
      cursor: pointer;
    }
  }
}


</style>
