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
    <div class="center-rule">
      <div class="cyan-rule"></div>
    </div>
  </main>
  <div class="boost-section">
    <div class="boost-cta">
      <h2>Boost your links today</h2>
      <a href="">Get Started</a>
    </div>
    <img
      src="../assets/images/bg-boost-mobile.svg"
      class="bg-boost-mobile"
      alt=""
    />
  </div>
  <FooterVue />
</template>

<script>
import StatisticsVue from "./Statistics.vue";
import FooterVue from "./Footer.vue";
export default {
  name: "Main",
  components: { StatisticsVue, FooterVue },
  data() {
    return {};
  },
};
</script>

<style scoped>
.container {
  background-color: #f0f1f6;
  height: 250vh;
  /* transform: translateY(-80px); */
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
  max-width: 100%;
  margin: 30px;
}
.center-rule {
  display: flex;
  align-items: center;
  justify-content: center;
}
.cyan-rule {
  width: 10px;
  height: 880px;
  background-color: hsl(180, 66%, 49%);
  position: absolute;
  transform: translateY(-300px) rotate(180deg);
  z-index: -1;
}
.boost-section {
  /* transform: translateY(-80px); */
  height: 300px;
  position: relative;
  background-color: hsl(257, 27%, 26%);
}
.boost-section .boost-cta {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  transform: translateY(100px);
}
.boost-section .boost-cta h2 {
  color: #fff;
  font-size: 30px;
  margin-bottom: 20px;
}
.boost-section .boost-cta a {
  padding: 15px 50px;
  color: #fff;
  font-size: 20px;
  border-radius: 50px;
  background-color: hsl(180, 66%, 49%);
  text-decoration: none;
}
.boost-section .bg-boost-mobile {
  position: absolute;
  z-index: -1;
  right: 0;
  top: 0;
}
@media (min-width: 720px) {
  .container {
    height: 200vh;
  }
  .card-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    transition: display 0.1s ease-in;
    max-width: 100%;
  }
  .cyan-rule {
    display: none;
  }
}
@media (min-width: 920px) {
  .container {
    height: 170vh;
  }
  .card-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    transition: display 0.1s ease-in;
    max-width: 100%;
  }
  .cyan-rule {
    display: block;
    position: absolute;
    transform: rotate(270deg);
    z-index: -1;
  }
}
</style>
