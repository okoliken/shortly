<template>
  <div class="card">
    <div class="icon-circle">
      <img src="../assets/images/icon-brand-recognition.svg" alt="" />
    </div>
    <div class="card-body">
      <h1>Brand recognition</h1>
      <p>
        Boost your band recognition with each click. Generic links don't mean a
        thing. Branded Links help instil confidence in your content
      </p>
    </div>
  </div>
  <div class="card step2">
    <div class="icon-circle">
      <img src="../assets/images/icon-detailed-records.svg" alt="" />
    </div>
    <div class="card-body">
      <h1>Detailed Records</h1>
      <p>
        Gain insights into who is clicking your links. Knowing when and where
        people engage with your content helps inform better decisions
      </p>
    </div>
  </div>
  <div class="card step3">
    <div class="icon-circle">
      <img src="../assets/images/icon-fully-customizable.svg" alt="" />
    </div>
    <div class="card-body">
      <h1>Fully Customizable</h1>
      <p>
        Improve brand awareness and content discoverability through customizable
        links, superchanging audience engagement
      </p>
    </div>
  </div>
</template>

<style scoped>
.card {
  background-color: #fff;
  border-radius: 10px;
  width: 100%;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  margin-bottom: 100px;
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
.card-body {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  text-align: center;
  padding: 26px;
  margin-top: -18px;
}
.card .card-body h1 {
  font-size: 25px;
  color: hsl(260, 8%, 14%);
  margin-bottom: 15px;
}
.card .card-body p {
  font-size: 17px;
  color: hsl(257, 7%, 63%);
}
@media (min-width: 920px) {
  .card-body {
    padding: 25px;
  }
  .step2 {
    transform: translateY(30px);
    transition: all 0.1s ease;
  }
  .step3 {
    transition: all 0.1s ease;

    transform: translateY(50px);
  }
}
</style>
