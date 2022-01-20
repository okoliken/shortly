<template>
  <div class="flex-url-header">
    <header class="url-shortner-header">
      <div class="url-shortner-logo">
        <img src="../assets/images/logo.svg" alt="" />

        <img
          @click="toggleMoblieNav"
          src="../assets/images/menu.png"
          alt=""
          class="menu"
        />
      </div>
      <ul class="desk-nav">
        <li><a href="">Features</a></li>
        <li><a href="">Pricing</a></li>
        <li><a href="">Resources</a></li>
      </ul>

      <transition name="slide" mode="out-in" style="position: absolute">
        <nav class="url-shortner-nav" v-show="showMoblieNav">
          <ul>
            <li><a href="">Features</a></li>
            <li><a href="">Pricing</a></li>
            <li><a href="">Resources</a></li>
            <li class="faint-line"></li>
            <li><a href="" class="login">Login</a></li>
            <li><a href="" class="cayn-blue">Sign up</a></li>
          </ul>
        </nav>
      </transition>
    </header>
    <ul class="desktop-register-links">
      <li><a href="" class="login-desktop">Login</a></li>
      <li><a href="" class="cayn-blue-desktop">Sign up</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMoblieNav: false,
    };
  },
  methods: {
    toggleMoblieNav() {
      this.showMoblieNav = !this.showMoblieNav;
    },
  },
};
</script>

<style scoped>
.slide-enter-active,
.slide-leave-active {
  transition: all 0.4s ease;
}
.slide-enter-from,
.slide-leave-to {
  opacity: 0;
  transform: translateY(30px);
}
.url-shortner-header {
  padding: 25px 15px;
}
.url-shortner-header .url-shortner-nav {
  width: 94%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 35px 3px;
  z-index: 10;

  margin: 18px 0 0 0;
  background-color: hsl(257, 27%, 26%);
  border-radius: 6px;
}
.url-shortner-header .url-shortner-logo {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.url-shortner-header .url-shortner-logo .menu {
  width: 28px;
  display: block;
  cursor: pointer;
}
.url-shortner-header .url-shortner-nav ul .faint-line {
  border-bottom: 1px solid hsl(0, 0%, 75%);
  width: 100%;
}
.url-shortner-header .url-shortner-nav ul {
  width: 100%;
  display: flex;
  padding: 0 12px;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.url-shortner-header .url-shortner-nav li {
  margin-bottom: 20px;
}
.url-shortner-header .url-shortner-nav li a {
  color: #fff;
  font-weight: 500;
  text-decoration: none;

  font-size: 20px;
}
.url-shortner-header .url-shortner-nav li a.cayn-blue {
  padding: 10px 100px;
  background-color: hsl(180, 66%, 49%);
  border-radius: 50px;
  display: block;
}
.url-shortner-header .url-shortner-nav li a.cayn-blue:hover {
  transition: all 0.1s ease-in;
  background-color: hsl(180, 76%, 40%);
}
.url-shortner-header .url-shortner-nav li a.login {
  display: block;
}
.desktop-register-links a.login-desktop {
  display: none;
}
.desktop-register-links a.cayn-blue-desktop {
  display: none;
}
.url-shortner-header .desk-nav {
  display: none;
}
@media (min-width: 720px) {
  .flex-url-header {
    display: flex;
    align-items: center;
    transition: all 1s ease;
    justify-content: space-between;
  }
  .url-shortner-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .url-shortner-header .url-shortner-nav {
    width: 100%;
    display: flex;
    background: none;
    flex-direction: row;
    justify-content: space-between;
    padding: 0;
  }
  .url-shortner-header .desk-nav {
    display: flex;
    margin-left: 15px;
    transition: display 0.1s ease;
  }
  .url-shortner-header .desk-nav li {
    margin-left: 10px;
  }
  .url-shortner-header .desk-nav a {
    color: hsl(0, 0%, 75%);
    text-decoration: none;
  }
  .url-shortner-header .url-shortner-logo .menu {
    display: none;
  }
  .url-shortner-header .url-shortner-nav ul .faint-line {
    display: none;
  }
  .url-shortner-header .url-shortner-nav ul {
    width: 100%;
    flex-direction: row;
    align-items: flex-end;
    justify-content: flex-end;
  }
  .url-shortner-header .url-shortner-nav li {
    margin-bottom: 20px;
  }
  .url-shortner-header .url-shortner-nav li a {
    color: hsl(255, 11%, 22%);
    font-weight: 500;
    text-decoration: none;

    font-size: 20px;
  }
  .url-shortner-header .url-shortner-nav li a.cayn-blue {
    display: none;
  }
  .url-shortner-header .url-shortner-nav li a.login {
    display: none;
  }
  .desktop-register-links {
    display: flex;
    align-items: center;
  }
  .desktop-register-links li {
    margin-right: 10px;
  }
  .desktop-register-links a {
    color: hsl(0, 0%, 75%);
    text-decoration: none;
  }
  .desktop-register-links a.login-desktop {
    display: block;
    transition: display 0.1s ease;
  }
  .desktop-register-links a.cayn-blue-desktop {
    display: block;
    padding: 8px 18px;
    border-radius: 50px;
    background-color: hsl(180, 66%, 49%);
    color: #fff;
    transition: display 0.1s ease;
  }
  .desktop-register-links a.cayn-blue-desktop:hover {
    transition: all 0.2s ease;
    background-color: hsl(180, 55%, 67%);
  }
}

@media (min-width: 920px) {
  .flex-url-header {
    padding: 30px 60px;
    transition: all 1s ease;
  }
  .url-shortner-header .desk-nav {
    margin-left: 30px;
    transition: all 1s ease;
  }
  .url-shortner-header .desk-nav li {
    margin-left: 24px;
    transition: all 1s ease;
  }
  .desktop-register-links li {
    transition: all 1s ease;
    margin-right: 40px;
  }
  .desktop-register-links {
    transition: all 1s ease;
    margin-right: 80px;
  }
}
</style>
