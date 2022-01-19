<template>
  <footer>
    <div class="col-01">
        <h4>Ceylon Info (pvt) Ltd</h4>
        <p>No-15, colombo 10</p>
        <p>Sri Lanka</p>
        </div>
    <div class="col-02">
      <h5>Follow Us</h5>
      <a href="https://www.facebook.com/"
        ><img src="../assets/images/social/facebook.png" alt=""
      /></a>
      <a href="https://twitter.com"
        ><img src="../assets/images/social/twitter.png" alt=""
      /></a>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
footer {
  margin: 10px 0 0 0;
  background-color: #42b983;
  height: 10rem;
  padding: 1rem;
  color: aliceblue;
  display: flex;
  align-content: center;
  align-items: center;
}

@media (max-width: 750px) {
    footer{
        display: flex;
        flex-direction: column;
    }
    
}

.col-01 {
  flex: 1;
  
}

.col-02 {
  flex: 1;
}
</style>
