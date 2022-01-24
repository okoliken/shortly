<template>
  <Navbar />
  <HeroSectionVue />
  <UrlShortenerVue @shortlink="getShortenedLinkFromApi" />
  <MainVue :shortenedLink="shortenedLink" />
</template>

<script>
import Navbar from "./components/Navbar.vue";
import HeroSectionVue from "./components/HeroSection.vue";
import UrlShortenerVue from "./components/UrlShortener.vue";
import MainVue from "./components/Main.vue";

export default {
  name: "App",
  components: {
    Navbar,
    HeroSectionVue,
    UrlShortenerVue,
    MainVue,
  },
  data() {
    return {
      shortenedLink: null,
    };
  },
  methods: {
    async getShortenedLinkFromApi(userinput) {
      console.log(userinput);
      try {
        const request = await fetch(
          `https://api.shrtco.de/v2/shorten?url=${userinput}`
        );
        const data = await request.json();
        console.log(data);
        this.shortenedLink = data;
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,500;1,500&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style-type: none;
}
body {
  font-family: "Poppins";
}
</style>
