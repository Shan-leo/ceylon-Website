<template>
  <div class="welcome">
    <span>Welcome To Sri Lanka</span>
    <img src="../assets/images/welcome.jpg" alt="" />
  </div>
</template>

<script>
export default {
  name: "Welcome",
};
</script>

<style scoped>
.welcome {
  margin: 0 ;
  position: relative;
  width: 100%;
}

span {
  color: white;
  font-size: 3em;
  width: 60%;
  position: absolute;
  top: 60%;
  left: 20%;
  margin-bottom: 1rem; 

  z-index: 10;
}

img {
  width: 100%;
  object-fit:cover;
  
}

@media (max-width:750px) {
  img{
    height:45vh ;
  }

  span {
  color: white;
  font-size: 1.9em;
  z-index: 10;
}
}
</style>
