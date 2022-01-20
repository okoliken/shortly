<template>
  <div class="card">
    <div class="icon-circle">
      <img src="../assets/images/icon-brand-recognition.svg" alt="" />
    </div>
    <div class="card-body">
      <h1>Brand recognition</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "Statistics",
};
</script>

<style scoped>
.card {
  background-color: #fff;
  border-radius: 10px;
  width: 100%;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
.card .icon-circle {
  width: 100px;
  height: 100px;
  transform: translateY(-50px);
  background-color: hsl(257, 27%, 26%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
