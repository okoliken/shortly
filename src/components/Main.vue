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
  </main>
</template>

<script>
import StatisticsVue from "./Statistics.vue";
export default {
  name: "Main",
  components: { StatisticsVue },
};
</script>

<style scoped>
.container {
  background-color: #f0f1f6;
  height: 100vh;
  transform: translateY(-80px);
  position: relative;
  z-index: -1;
}
.container_statistics {
  text-align: center;
  transform: translateY(190px);
  transition: all 0.2s ease-in;
}
.container_statistics h1 {
  margin-bottom: 26px;
  transition: all 0.2s ease-in;
}
.container_statistics p {
  font-size: 20px;
  color: hsl(257, 7%, 63%);
}
.card-container {
  transform: translateY(290px);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
</style>
