<template>
  <footer>
    <div class="footer-shortly">
      <div class="f-logo">
        <h1 class="logo">Shortly</h1>
      </div>
      <div class="features">
        <p>Features</p>
        <div class="links">
          <a href="">Link Shortening</a>
          <a href="">Branded Links</a>
          <a href="">Analytics</a>
        </div>
      </div>

      <div class="Resources">
        <p>Resources</p>
        <div class="links">
          <a href="">Blog</a>
          <a href="">Developers</a>
          <a href="">Support</a>
        </div>
      </div>

      <div class="Company">
        <p>Company</p>
        <div class="links">
          <a href="">About</a>
          <a href="">Our Team</a>
          <a href="">Careers</a>
          <a href="">Contact</a>
        </div>
      </div>

      <div class="socials">
        <img src="../assets/images/icon-facebook.svg" alt="" />
        <img src="../assets/images/icon-twitter.svg" alt="" />
        <img src="../assets/images/icon-pinterest.svg" alt="" />
        <img src="../assets/images/icon-instagram.svg" alt="" />
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
.footer-shortly {
  background: #232027;
  padding: 30px;
  /* height: 110vh; */
  text-align: center;
}
.footer-shortly .f-logo {
  margin-bottom: 50px;
}
.footer-shortly .f-logo .logo {
  color: #fff;
  font-weight: 700;
  font-size: 30px;
}
.footer-shortly .features,
.Resources,
.Company {
  margin-bottom: 40px;
}
.footer-shortly .features,
.Resources,
.Company p {
  color: #fff;
  font-size: 20px;
}
.footer-shortly .links {
  display: flex;
  align-items: center;
  flex-direction: column;
}
.footer-shortly .links a {
  text-decoration: none;
  font-size: 17px;
  margin-top: 10px;
  color: hsl(257, 7%, 63%);
}
.socials {
  margin-bottom: 10px;
}
.socials img {
  width: 30px;
  margin-left: 10px;
}
@media (min-width: 1024px) {
  .footer-shortly .f-logo {
    margin-bottom: 0;
  }
  .footer-shortly {
    height: 400px;
    padding-top: 100px;
    display: grid;
    transition: all 0.1s ease;
    grid-template-columns: repeat(5, 1fr);
  }
}
</style>
