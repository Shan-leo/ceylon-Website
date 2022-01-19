<template>
  <header>
    <nav class="container">
      <div class="brand">
        <router-link class="logo" :to="{ name: 'Home' }">Pearl Of Indian Ocean</router-link>
      </div>
      <div class="links">
        <ul v-show="!mobile">
          <router-link class="link" :to="{ name: 'Home' }">Home</router-link>
          <router-link class="link" :to="{ name: 'Blog' }">Blog</router-link>
          <router-link class="link" :to="{ name: 'About' }"
            >About Us</router-link
          >
          <router-link class="link" :to="{ name: 'ContactUs' }"
            >Contact Us</router-link
          >
        </ul>
      </div>
    </nav>
    <menuIcon @click="toggleMobileNav" class="menu-icon" v-show="mobile" />
    <img
      src="../assets/images/bars.png"
      alt=""
      @click="toggleMobileNav"
      class="menu-icon"
      v-show="mobile"
    />

    <transition name="mobile-nav">
      <ul class="mobile-nav" v-show="mobileNav">
        <router-link class="link" :to="{ name: 'Home' }">Home</router-link>
        <router-link class="link" :to="{ name: 'Blog' }">Blog</router-link>
        <router-link class="link" :to="{ name: 'About' }">About Us</router-link>
        <router-link class="link" :to="{ name: 'ContactUs' }"
          >Contact Us</router-link
        >
      </ul>
    </transition>
  </header>
</template>

<script>
export default {
  name: "Navigation",
  components: {},

  data() {
    return {
      mobile: null,
      mobileNav: null,
      windowWidth: null,
    };
  },

  created() {
    window.addEventListener("resize", this.checkScreen);
    this.checkScreen();
  },

  methods: {
    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 750) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    },

    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
}

.brand {
  flex: 2;
}
.logo {
  text-decoration: none;
  font-size: 2rem;
  font-weight: 700;

  
}

.links {
  flex: 7;
}

.link {
  padding: 0 7px;
  font-size: 1.2rem;
  text-decoration: none;
  font-weight: bold;
}

.link:hover {
  font-size: 1.3rem;
}

.mobile-nav {
  padding: 20px;
  width: 70%;
  max-width: 250px;
  display: flex;
  flex-direction: column;
  position: fixed;
  height: 100%;
  background-color: #303030;
  top: 0;
  left: 0;
  z-index: 99;
}

.mobile-nav > .link {
  color: antiquewhite;
  padding: 15px;
}
.mobile-nav-enter {
  transform: translateX(-250px);
}

.menu-icon {
  cursor: pointer;
  position: absolute;
  top: 25px;
  right: 25px;
  height: 25px;
  width: auto;
}

@media (max-width:740px) {
  
  .logo{
    font-size: 1rem;
  }
    
  }
</style>
