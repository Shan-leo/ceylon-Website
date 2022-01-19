<template>
  <div class="card">
    <router-link class="link" :to="{ name: 'Details' }">
      <img :src="require(`../assets/images/provinces/${post.image}`)" alt="" />
      <p>{{ post.title }}</p>
    </router-link>
  </div>
</template>

<script>
export default {
  name: "ProvinceCard",
  props: ["post"],
};
</script>

<style scoped>
.card {
  width: 300px;
  height: 230px;
  border-style: solid;
  margin: 0.5rem;
  background-color: #42b983;
}
img {
  width: 300px;
  height: 190px;
}

p {
  font-size: 1.3rem;
  color: aliceblue;
  font-weight: bold;
  text-decoration: none;
}
.link {
  text-decoration: none;
}
</style>
