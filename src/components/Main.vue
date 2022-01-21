<template>
  <main class="container">
    <div class="container_statistics">
      <h1>Advanced Statistics</h1>
      <p>
        Track how your links are performing across the web our advanced
        statistics dashboard.
      </p>
    </div>
    <div class="card-container">
      <StatisticsVue />
    </div>
    <div class="cyan-rule"></div>
  </main>
</template>

<script>
import StatisticsVue from "./Statistics.vue";
export default {
  name: "Main",
  components: { StatisticsVue },
  data() {
    return {};
  },
};
</script>

<style scoped>
.container {
  background-color: #f0f1f6;
  height: 200vh;
  transform: translateY(-80px);
  position: relative;
  z-index: -1;

  padding: 10px;
}
.container_statistics {
  text-align: center;
  transform: translateY(190px);
  transition: all 0.2s ease-in;
}
.container_statistics h1 {
  margin-bottom: 26px;
  transition: all 0.2s ease-in;
  color: hsl(260, 8%, 14%);
}
.container_statistics p {
  font-size: 20px;
  color: #9e9aa7;
}
.card-container {
  transform: translateY(290px);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  margin: 30px;
}
.cyan-rule {
  width: 10px;
  height: 880px;
  background-color: hsl(180, 66%, 49%);
}
@media (min-width: 720px) {
  .card-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    transition: display 0.1s ease-in;
  }
}
@media (min-width: 920px) {
  .card-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    transition: display 0.1s ease-in;
  }
  .cyan-rule {
    position: absolute;
    transform: translateY(-450px) translateX(500px) rotate(270deg);
    z-index: -1;
  }
}
</style>
