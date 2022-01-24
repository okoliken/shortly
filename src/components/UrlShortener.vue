<script>
export default {
  name: "UrlShortener",
  data: () => {
    return {
      shortenUrlLinks: "",
      isEmpty: false,
    };
  },
  methods: {
    getUrlLinksFromSearchInput() {
      if (this.shortenUrlLinks === "") {
        this.isEmpty = true;
        setTimeout(() => {
          this.isEmpty = false;
        }, 2000);
      } else {
        this.$emit("shortlink", this.shortenUrlLinks);
      }
    },
  },
};
</script>

<template>
  <div class="center-url-con">
    <div class="url-shortener-container">
      <form class="url-shortener-form">
        <div class="url-input-con">
          <input
            :class="[isEmpty === true ? 'red-input-border' : '']"
            type="text"
            class="shortener"
            placeholder="Shorten a Link here..."
            v-model="shortenUrlLinks"
          />
          <transition name="slide-in" mode="out-in">
            <span v-if="isEmpty" class="red-error-text">Please add a link</span>
          </transition>
        </div>
        <a @click="getUrlLinksFromSearchInput" class="url-btn">Shorten It!</a>
      </form>
    </div>
    <img class="light-bg" src="../assets/images/bg-shorten-mobile.svg" alt="" />
    <img
      src="../assets/images/bg-shorten-desktop.svg"
      alt=""
      class="light-bg-deskktop"
    />
  </div>
</template>

<style scoped>
.slide-in-enter-active,
.slide-in-leave-active {
  transition: opacity 0.4s ease;
}
.slide-in-enter-from,
.slide-in-leave-to {
  opacity: 0;
}
.url-shortener-form input.red-input-border {
  border: 2px solid hsl(0, 87%, 67%);
  transition: all 0.2s ease;
}
span.red-error-text {
  color: hsl(0, 87%, 67%);
  font-style: italic;
  z-index: 10;
  transform: translateY(67px);
  position: absolute;
  transition: all 0.2s ease;
}
.center-url-con {
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  overflow: hidden;
  position: relative;
  transform: translateY(70px);
  margin: 68px 20px 0 20px;
  height: auto;
  justify-content: center;
  border-radius: 10px;
  background-color: hsl(257, 27%, 26%);
}
.url-shortener-container {
  width: 100%;
  padding: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.light-bg-deskktop {
  display: none;
}
.url-shortener-form {
  z-index: 10;
  width: 100%;
  transform: translateY(-4px);
}
.url-shortener-form input {
  width: 100%;
  padding: 14px;
  box-sizing: border-box;
  appearance: none;
  border: none;
  font-family: "poppins";
  font-size: 18px;
  border-radius: 10px;
  margin: 10px 0 20px 0;
}
.url-shortener-form a {
  display: block;
  width: 100%;
  padding: 10px 12px;
  text-align: center;
  color: #fff;
  font-weight: bold;
  font-size: 20px;
  outline: none;
  border-radius: 10px;
  background-color: hsl(180, 66%, 49%);
}
.url-shortener-form a:hover {
  cursor: pointer;
}
.light-bg {
  position: absolute;
  top: 0;
  right: 0;
}
.url-shortener-form .url-input-con {
  display: flex;
  position: relative;
  flex-direction: column;
}
@media (min-width: 720px) {
  .center-url-con {
    display: flex;
    padding: 30px;
    transform: translateY(90px);
    margin: 68px 40px;
  }
  .url-shortener-form {
    display: flex;
    z-index: 100;
    transition: all 0.1s ease-in-out;
    align-items: center;
    justify-content: space-between;
    width: 100%;
  }
  .url-shortener-form input {
    margin: 0;
    flex: 4;
    width: 100%;
    padding: 14px;
    transition: all 0.1s ease-in-out;
  }

  .url-shortener-form .url-input-con {
    flex: 4;
  }
  .url-shortener-form .url-input-con span {
    display: inline;
  }
  .url-shortener-form a.url-btn {
    margin: 4px;
    flex: 2;
    padding: 14px 7px;
    font-size: 18px;
    transition: all 0.1s ease-in-out;
  }
  .light-bg-deskktop {
    display: block;
    position: absolute;
    bottom: 2px;
    /* z-index: -1; */
    left: 0;
  }
  .url-shortener-form a.url-btn:hover {
    transition: all 0.2s ease;
    background-color: hsl(180, 55%, 67%);
    cursor: pointer;
  }
}
@media (min-width: 920px) {
  .center-url-con {
    margin: 68px 150px 30px 58px;
    transition: all 0.1s ease-in-out;
    height: 170px;
  }
  .url-shortener-form input {
    padding: 17px;
    transition: all 0.1s ease-in-out;
    font-size: 22px;
    outline: none;
  }

  .url-shortener-form a.url-btn {
    flex: 1;
    transition: all 0.1s ease-in-out;
    padding: 19px;
    margin-left: 6px;
  }
}
</style>
