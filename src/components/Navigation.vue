<template>
  <header>
      <nav class="container">
          <div class="brand">
              <router-link class="logo" to="{name:'Home'}">Ceylon</router-link>
          </div>
          <div class="links">
              <router-link class="link" :to="{name:'Home'}">Home</router-link>
              <router-link class="link" :to="{name:'Blog'}">Blog</router-link>
              <router-link class="link" :to="{name:'About'}">About Us</router-link>
              <router-link class="link" :to="{name:'ContactUs'}">Contact Us</router-link>
          </div>
      </nav>
  </header>
</template>

<script>
export default {
    name:'Navigation',

}
</script>

<style scoped>
.container{
    display: flex;
}

.brand{
    flex: 2;
}
.logo{
    text-decoration: none;
    font-size: 2rem;
    font-weight: 700;

}

.links{
    flex: 7;
}

.link{
    padding: 0 7px;
    font-size: 1.2rem;
    text-decoration: none;
    font-weight: bold;
}

.link:hover{
    font-size: 1.3rem;
}


</style>
