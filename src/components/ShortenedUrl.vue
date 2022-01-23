<script>
export default {
  name: "ShortenedUrl",
  data() {
    return {};
  },
};
</script>

<template>
  <div class="container-liks">
    <div class="shortened-urls">
      <div class="raw-url">
        <h2 class="users-url">https://github.com</h2>
      </div>
      <div class="shortened-con">
        <p class="shortened-url">https://github.com</p>
        <a href="#" class="copy-link-btn">Copy</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container-liks {
  transform: translateY(100px);
  margin: 0 20px 8px 20px;
}
.shortened-urls {
  background-color: #fff;
  border-radius: 10px;
}
.shortened-urls .users-url {
  font-size: 18px;
  font-weight: 520;
}
.shortened-urls .raw-url {
  color: hsl(257, 27%, 26%);
  padding: 10px;
  border-bottom: 0.8px solid hsl(257, 7%, 63%);
}
.shortened-con {
  padding: 10px;
}
.shortened-con .shortened-url {
  color: hsl(180, 66%, 49%);
  margin-bottom: 10px;
}
.shortened-con .copy-link-btn {
  outline: none;
  appearance: none;
  padding: 12px 30px;
  border: none;
  color: #fff;
  border-radius: 10px;
  text-decoration: none;
  font-weight: 700;
  background-color: hsl(180, 66%, 49%);
}

@media (min-width: 720px) {
  .container-liks {
    margin: 0 40px;
  }
  .shortened-urls {
    display: flex;
    height: 80px;
    align-items: center;
    justify-content: space-between;
  }
  .shortened-urls .raw-url {
    border-bottom: none;
  }
  .shortened-con {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .shortened-con .shortened-url {
    margin-bottom: none;
  }
}
@media (min-width: 920px) {
  .container-liks {
    margin: 0px 150px 8px 58px;
  }
  .shortened-urls .users-url {
    font-size: 23px;
  }
  .shortened-con .shortened-url {
    font-size: 23px;
    margin-right: 8px;
  }
}
</style>
