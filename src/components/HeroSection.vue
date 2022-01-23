<template>
  <div class="hero-section">
    <div class="img-con">
      <img
        class="hero-img"
        src="../assets/images/illustration-working.svg"
        alt=""
      />
    </div>
    <div class="hero-text">
      <h1>More than just shorter links</h1>
      <p>
        Build your brand's recognition and get detailed <br />
        insights on how your links are performing
      </p>

      <a href="" class="cyan-btn">Get Started</a>
    </div>
  </div>
</template>

<style scoped>
.hero-section {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.img-con {
  width: 100%;
  overflow-x: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}
.img-con .hero-img {
  object-fit: contain;
  max-width: 480px;

  /* width: 100%; */
  transform: translateX(80px);
}
.hero-section .hero-text {
  text-align: center;
  margin: 29px 0;
  padding: 5px;
}
.hero-section .hero-text h1 {
  font-size: 45px;
  font-weight: bold;
  color: hsl(260, 8%, 14%);
  line-height: 44px;
  margin-bottom: 16px;
}
.hero-section .hero-text p {
  color: hsl(257, 7%, 63%);
  line-height: 26px;
  font-size: 20px;
  margin-bottom: 36px;
}
.hero-section .hero-text .cyan-btn {
  padding: 13px 40px;
  background-color: hsl(180, 66%, 49%);
  color: #fff;
  font-size: 25px;
  text-decoration: none;
  border-radius: 50px;
}
@media (min-width: 920px) {
  .hero-section {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: row-reverse;
  }
  .hero-section .hero-text {
    text-align: justify;
    transform: translateX(60px);
    transition: all 1s ease;
  }
  .hero-section .hero-text h1 {
    font-size: 48px;
    letter-spacing: 0.3;
    font-weight: bold;
    color: hsl(260, 8%, 14%);
    line-height: 80px;

    transition: all 1s ease;
  }

  .img-con .hero-img {
    object-fit: contain;
    max-width: 600px;

    /* width: 100%; */
    transition: all 1s ease;
    margin-top: 40px;
    transform: translateX(100px);
  }
  .hero-section .hero-text .cyan-btn {
    transition: all 1s ease;
    font-size: 18px;
  }
  .hero-section .hero-text p {
    color: hsl(257, 7%, 63%);
    line-height: 28px;
    font-size: 17px;
    margin-bottom: 38px;
  }
}
@media (min-width: 1150px) {
  .hero-section {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: row-reverse;
  }
  .hero-section .hero-text {
    text-align: justify;
    transform: translateX(60px);
    transition: all 1s ease;
  }
  .hero-section .hero-text h1 {
    font-size: 78px;
    letter-spacing: 0.3;
    font-weight: 800;
    color: hsl(260, 8%, 14%);
    line-height: 80px;

    transition: all 1s ease;
  }

  .img-con .hero-img {
    object-fit: contain;
    max-width: 800px;

    /* width: 100%; */
    transition: all 1s ease;
    margin-top: 40px;
    transform: translateX(100px);
  }
  .hero-section .hero-text .cyan-btn {
    transition: all 1s ease;
    padding: 13px 40px;
    font-size: 22px;
  }
  .hero-section .hero-text .cyan-btn:hover {
    transition: all 0.2s ease;
    background-color: hsl(180, 55%, 67%);
  }
  .hero-section .hero-text p {
    color: hsl(257, 7%, 63%);
    line-height: 38px;
    font-size: 20px;
    margin-bottom: 38px;
  }
}
</style>
