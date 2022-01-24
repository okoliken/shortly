<script>
export default {
  name: "ShortenedUrl",
};
</script>

<template>
  <div class="container-liks">
    <div class="shortened-urls">
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.container-liks {
  transform: translateY(100px);
  margin: 0 5px 8px 5px;
}
.shortened-urls {
  background-color: #fff;
  border-radius: 10px;
  width: auto;
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
}
@media (min-width: 920px) {
  .container-liks {
    margin: 0px 150px 8px 58px;
  }
}
</style>
